+++
title = 'Architektura (nejen) C# projektu 2'
date = 2022-05-21T12:00:00+02:00
draft = false
+++
## Architektura souběžností
Jak jsem psal v předchozím díle, programátor by neměl používat transakční mechanismus databáze (např. SQL transakce) a za souběžnosti a zamykání dat před validací a zápisem by měl vzít zodpovědnost ve svém kódu napřímo.

Jak to ale udělat? Je vůbec možné vymyslet univerzální architekturu pro zpracování souběžností? Nebo je nutné analyzovat každou doménu zvlášť?

## Čtení
V prostředí businessových API aplikací je nutné se na každý kus kódu dívat z pohledu škálovatelnosti a předpokládat, že každý řádek může běžet souběžně na 10 serverech a na každém serveru v 1000 vláknech (10×1000).

Konkrétní hodnoty nejsou důležité. 10×1000 může být v kontextu jedné aplikace zátěžový test, v kontextu jiné aplikace může jít o produkční provoz. O to nejde.

Pokud na API přistál request na čtení dat, je nám úplně jedno, kolik serverů a kolik vláken čtení obsluhuje. Díky tomu je čtení pro nás programátory ta jednodušší část kódu. Nemusíme vytvářet žádné zámky a prakticky jen delegujeme čtecí requesty na náš databázový systém, ať už jde o SQL data nebo NoSQL dokumenty (jsme v eventuální konzistenci).

## Zápis
Pokud na API přistál request na zápis dat, je zamykání složitější. V jakém rozsahu se má zamykat? Na to existuje několik možností a všechny jsou validní, záleží na kontextu.

Příklad: mám 2 typy agregátů, Order (objednávka) a Product (produkt).

- **Plošný zámek pro jakýkoliv zápis**: všechny operace pro zápis používají jeden zámek.
  - Jakmile jeden uživatel provede nějakou změnu dat, všechny ostatní requesty musí čekat bez ohledu na to, zdali jde o změnu v objednávce nebo v produktu.
  - Může se zdát, že takovýto režim zamykání je absolutně nesmyslný. Berte ale na vědomí, že implementovat plošný zámek pro zápis je velmi triviální a například u POCů a malých aplikací může dávat smysl.
- **Zámek nad typem agregátu**: všechny operace pro zápis nad konkrétním typem agregátu používají jeden zámek.
  - Toto znamená, že lze souběžně změnit jakýkoliv Order a jakýkoliv Product ale už nelze souběžně změnit 2 různé Ordery.
  - Typ agregátu je z definice nezávislý na ostatních typech tzn. Order je zcela nezávislý na Product.
  - Tento typ zámku nedává dle mého názoru moc velký smysl. Implementačně je složitější a DDD již zaručuje izolaci na úrovni instance agregátu. Proto je lepší typ 3 níže.
- **Zámek nad instancí agregátu**: všechny operace pro zápis nad konkrétní instancí agregátu používají jeden zámek.
  - Toto znamená, že lze souběžně změnit 2 různé Ordery, nezávisle na sobě a na jakémkoliv jiném agregátu, např. na Productu.
  - Není však možné provádět souběžně 2 operace na jednom Orderu, na jedné objednávce.
  - Zamykání nad instancí agregátu lidem často připomíná aktory, v předchozím článku ale pojmenovávám důvody, proč je lepší se aktorům vyhnout.
- **Detailní manipulace se zámky v instanci agregátu v závislosti na business logice**
  - V rámci jedné instance agregátu je možné provádět souběžně doménovou logiku, která provádí zápis dat. Např. první metoda/handler aktualizuje informaci Order.State (stav objednávky) zatímco jiná metoda/handler aktualizuje informaci Order.CustomerNote (poznámka zákazníka). Z businessové logiky to dává smysl, není třeba zamykat stav objednávky, pokud dochází k aktualizaci poznámky zákazníka.
  - Implementace na takto podrobné úrovni by dle mého názoru měla probíhat pouze na základě reálného optimalizačního požadavku. Jinými slovy, pokud v provozu existují reálné problémy s tím, že se uživatelům nedaří něco změnit.
    - Většinu času by toto neměl být problém, protože víme, že u většiny businessů je ~80% operací čtení a pouze ~20% operací je zápis, rozložený napříč všemy instancemi agregátů.
    - **POZOR**: Pokud nad jednou instancí agregátu potřebuje pracovat v jednom čase velké množství lidí, pak je možné, že jsme blbě navrhli doménu. Pokud vznikne objednávka a s touto objednávkou – konkrétní instancí agregátu Order – potřebují pracovat zpracovatel objednávek, skladník, účetní, dispečer atd. pak je zjevné, že naše doména není úplně dobře vymyšlená. (Zpracovatel by měl pracovat se stavem objednávky, skladník se skladovými zásobami/výdejkami, účetní s doklady, dispečer s dopravci, helpdesk se zákazníkem atd.)

## „Distribuované zámky“

V doménové architektuře je doménová logika rozsekána mezi jednotlivé agregáty. User, Product, atd. Každý agregát obsahuje metody/handlery, které obsluhují jednotlivé commandy/requesty.

Dle mého názoru je se vyplatí už od začátku implementovat zámky nad konkrétní instancí agregátu (v předchozí kapitole bod 3.). Tyto zámky musí být implementovány jako distribuované zámky. Jen pozor, že velmi často pojem „distribuovaný zámek“ (v angličtině „distributed lock“) může znamenat jednu z následujících věcí:

- Zámek, který je používán distribuovanou aplikací (= o čem píšu)
 - Zámek, který je distribuován na více serverech/instancích (např. redis skrz redlock algoritmus)

Pochopitelně zámek používáný distribuovanou API může a nemusí být sám distribuovaný (běžet na více serverech a instancích).

## Zámek v agregátu a v ságách

V DDD je každá změna vyvolaná nějakým konkrétním commandem/requestem a tato změna je zpracována konkrétní metodou agregátu nebo handlerem. V mé architektuře to je MediatRovský handler.

Request handler náležící konkrétnímu agregátu je izolovaný od všeho ostatního a pracuje pouze s daty konkrétní instance agregátu. Před provedením metody musí dojít k uzamčení celého agregátu tzn. vytvoříme zámek s identifikátorem např. Product_123 kde 123 je identifikátor produktu.

![Zamkovani](/it-blog/architektura-projektu2-diag.png)

V ságách probíhá redistribuce příkazů napříč více agregáty. Už na úrovni agregátu je však velmi často nutné řešit zámky!

Příklad: mějme operaci CreateOrder která vytváří objednávku. Musí se zamknout několik agregátů najednou ještě před tím, než sága začne vytvářet příkazy na jednotlivé handlery.

- *DiscountVoucher* – slevový kupón, který je v objednávce použitý
- *ProductItem* – skladová zásoba zakoupeného produkt
- *Order* – může být potřeba zamknout objednávku samotnou v závislosti na granulitě naší domény. Pokud objednávce stačí jeden command pak ji není třeba zamykat, košaté objekty jako Order mají ale tendenci mít spoustu dalších připojených dat, které se vkládají ne najednou ale až po vytvoření.

Nyní nám ale vzniknul problém. Pokud sága vytváří sama svoje zámky, dostává se do konfliktu s vytvářením zámků přímo v agregátech. Pokud si sága vytvoří zámek nad Order ale pak pro Order zavolá příkaz, v rámci RequestHandleru pro Order dojde k deadlocku.

![Deadlock](/it-blog/architektura-projektu2-deadlock.png)


V naší architektuře potřebujeme vědět, že pokud tvoříme zámek v rámci agregátu, musíme zkontorlovat, jestli ten samý zámek na ten samý klíč není vytvořen už ságou. Pokud ano, nic nezamykáme a volání na redis přeskočíme. Tuto kontrolu stačí provést v rámci requestu.