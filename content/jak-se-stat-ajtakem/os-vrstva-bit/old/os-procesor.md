---
draft: true
title: Virtuální paměť
weight: 2060
---

V nějaké kapitole o procesorech jsem se zmiňoval, že moderní procesory jsou stavěné pro software. Většina procesorů počítá s tím, že na nich poběží operační systém.

Toto bych rád rozvinul trochu víc do detailu protože si myslím, že je důležité pochopit, jak operační systém s procesorem interaguje a co to znamená pro člověka, který s operačním systémem pracuje.

## Co všechno může procesor dělat

Už byste z předchozích kapitol měli vědět, že procesor je hlava a srdce celého počítače které komunikuje s ostatními komponentami.

Co to znamená?

To znamená, že procesor obsahuje instrukce, které na signální úrovni interagují se všemi těmi zařízeními okolo sebe.

To je první důvod, proč je těžké napsat vlastní operační systém. OS obstarává instrukce v procesoru, které interagují s ostatními zařízeními a před obyčejným uživatelem schovává obrovskou složitost a komplexitu těchto interakcí. Různá zařízení mají celou řadu různých „protokolů“ a „kódů“ se kterými komunikují a operační systém na to musí být připravený, jinak se procesor se zařízeními okolo sebe nedorozumí.

Kromě toho, při špatném nebo zlomyslném použití těchto instrukcí je možné počítač nebo jeho komponenty fyzicky zničit!

## Režim procesoru

Instrukce procesoru jsou proto rozdělené na dvě kategorie:

- privilegovaný režim = ty instrukce, ke kterým má přístup jen operační systém. Jedná se hlavně o instrukce, které nějakým způsobem řídí interakce s ostatním hardwarem v počítači.
- uživatelský režim = všechny ostatní instrukce

Při startu počítače si operační systém v procesoru nastaví sám pro sebe privilegovaný režim. Jakýkoliv software, který běží v rámci operačního systému k těmto instrukcím nemá vůbec žádný přístup nebo pouze zprostředkovaně přes operační systém.

Co z toho plyne?

Pokud chce aplikace pracovat nějakým způsobem s různými zařízeními, musí to udělat prostřednictvím operačního systému.

Pokud tedy například programátor chce uložit něco do RAM paměti, detekovat stisk klávesy na klávesnici a podobně, musí si tyto interakce vykomunikovat s operačním systémem.

<div class="note1">

Programátory s orientací na software přímý přístup do konkrétního zařízení zpravidla ani nezajímá.

</div>

### Ovladač (driver)

Operační systém nemůže znát všechny typy zařízení, které na světě existují a nemůže být zodpovědný za všechny interakce v privilegovaném režimu. Proto mají operační systémy zabudovaný koncept ovladačů nebo driverů, které mají možnost přistupovat k privilegovaným instrukcím procesoru.

Proto je nutné si dávat hodně bacha na to, jaké ovladače si na počítač instalujete a operační systém se vás většinou jasně zeptá, jestli si jste fakt jisti, že chcete nějaký ovladač instalovat protože, teroeticky, jakýkoliv ovladač může váš počítač zničit. Prakticky toto není pro většinu uživatelů problém, OS v dnešní době vědí, jak komunikovat i s těmi nejběžnějšími komponentami.

Taky je to tím, že zníčit počítač tímto způsobem vyžaduje obrovské znalosti, které baseballová pálka nevyžaduje.

## Shrnutí

- Instrukce procesoru lze napsat tak, že dojde k fyzickému poškození komponent v počítači
- Z toho důvodu se instrukce dělí na několik režimů: privilegovaný a uživatelský režim
- Operační systém má přístup k privilegovanému režimu. Aplikace pouze k uživatelskému režimu.
- Pokud chce aplikace provést nějakou operaci v nějaké komponentě počítače, musí to udělat skrz funkce operačního systému.
- Ovladač je software, který umožňuje správnou interakci procesoru s nějakým zařízením, se kterým OS neumí jinak komunikovat