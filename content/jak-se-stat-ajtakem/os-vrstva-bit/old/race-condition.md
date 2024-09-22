---
draft: true
title: Race condition
weight: 2080
---

V minulém díle jsem mluvil o tom, že procesor pomocí context switchingu přepíná mezi jednotlivými běžícími vlákny.

Otázka za 5 bludišťáků: lze přesně určit, které běžící vlákno doběhne dříve?

Odpověď: Prakticky nelze.

Je to dáno několika faktory:

- První jednoduché procesory zpracovávaly instrukce napřímo, dnešní moderní procesory vykonávají jednotlivé instrukce v několika krocích v tzv. pipeline. V jednotlivých krocích pipelajny probíhají různé komplexní operace, včetně predikcí kdy se procesor snaží uhádnout výsledek instrukce (nebo následující instrukci) ještě před tím, než je instrukce spuštěna a to na základě krátkodobé statistiky, kterou si procesor ke spuštěným instrukcím udržuje. Délka této pipeliny je mezi 5 až 30 kroky. Vzhledem k prediktivním pipelajnám nelze odhadnout, jak daná instrukce proběhne rychle.
- Context switching ovlivňují všechny možné faktory od typu operačního systému, aktuálního zatížení procesoru, počtu běžících procesů atd. apod.
- Moderní procesory obsahují více jader, každé jádro obsahuje svoji vlastní pipelajnu.
- Moderní procesory umí regulovat svoji frekvenci (pro ekonomický provoz) a umí to dokonce pouze pro konkrétní vlákna
- Různé instrukce trvají různě dlouho. Procesor má sice jednu danou frekvenci např. 5 GhZ, jenže toto nelze převést přímo na počet instrukcí, i když to pro zjednodušení stačí.
- 5 GhZ znamená, že procesor zvládne 5 miliardů „ticků“ za vteřinu a různé instrukce procesoru mají odlišný počet ticků, za který se dokončí.

A nyní se dostáváme k tomu, co je Race condition – v češtině překládáno jako „souběh“ ale nikdy jsem neslyšel žádného ajťáka, který by tomu takhle říkal.

Race condition je jakákoliv situace, kdy máte minimálně dvě běžící vlákna a nevíte, které skončí dřív. Je prakticky nepředvídatelné, které vlákno z libovolného počtu běžících vláken skončí jako první.

<div class="blue-note">

Příklad ad absurdum:

Řekněme, že máte aplikaci, která obsahuje hlavní vlákno a jedno vedlejší, celkem 2 vlákna

1. vlákno obsahuje instrukci Počkej 100 vteřin.
Po 100 vteřinách vlákno skončí a zanikne.

2. vlákno obsahuje instrukci Počkej 1 vteřinu
Po 1 vteřině vlákno skončí a zanikne

Nyní chcete změřit, které vlákno skončí dřív.

Toto se zdá, jako absurdní příklad, že? Samozřejmě, že 2. vlákno skončí dřív. A v 99,99% případů to nejspíš i tak bude.
Jenže nemáte 100% záruku!

A to je ta pointa: bez použití dalších technik (o kterých budu psát později) nemáte nikdy 100% záruku, že nějaké vlákno skončí dřív, než to první.

V počítači se totiž kdykoliv může stát například něco takového:

– Spustí se vlákno A – počkej 1 vteřinu
– Spustí se vlákno B – počkej 100 vteřin
– Vlákno A je přiřazené k jádru X
– Vlákno B je přiřazené k jádru Y
– V jádru X však právě teď probíhá proces z úplně jiného vlákna patřícímu jinému procesu. Toto vlákno obsahuje výpočetně náročné instrukce a OS se rozhodne, že toto vlákno musí nejdřív doběhnout a že v rámci jádra X nepřidělí čas žádnému jinému vláknu.
– Na jádru Y žádné náročné procesy neprobíhají a vlákno B tedy spokojeně běží a odpočítává 100 vteřin.
– Za 100 vteřin skončí vlákno B
– Za 863 vteřin skončí zahlcení procesoru, proces skončil.
– Za 863.02 vteřiny začne vlákno A odpočítávat jednu vteřinu
– Za 864.02 vteřiny skončí vlákno A

</div>

Jednoduchá poučka zní: pokud potřebujete při programování aplikací zjistit, které vlákno doběhne dřív, děláte něco špatně. Samozřejmě v programování existují techniky, ve kterých můžete vlákna synchronizovat takže třeba můžete v jednom vlákně říct, že v určitém bodě musí jedno vlákno počkat, dokud se něco nestane v druhém vlákně. O tom ale budu psát až se budeme učit programovat.

Pokud neprovádíte nějakou formu synchronizace, vlákna běží v nepředvídatelném čase a nelze určit, která instrukce ve kterém vlákně proběhne dřív.

## Souhrn

- Race condition je pojmenování situace, kdy se snažíte zjistit, které vlákno doběhne dřív.
- Kdy které vlákno doběhne nelze (bez dalších technik jako např. synchronizace) předvídat.
- Běžící vlákna lze různými způsoby synchronizovat ale bez této synchronizace nelze určit, která instrukce ve kterém vlákně proběhne dřív.
- Běžící vlákna, která nejsou synchronizována, lze připodobnit k závodu formulí v mlze, který sledujete z tribuny na cílové čáře. Vidíte start a vidíte, kdo do cíle dojel dřív. Nemáte ale žádnou možnost jakkoliv ovlivnit, který z jezdců formule bude rychlejší, zkušenější a nebo který má lepší formuli.