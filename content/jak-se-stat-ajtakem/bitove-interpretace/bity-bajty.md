---
draft: false
title: Bajty
weight: 7020
---

Bajty, kilobajty, gigabajty, atd. jsou měrnou jednotkou bitů stejně jako centimetry, metry a kilometry jsou měrnou jednotkou vzdálenosti.

## byte (čti: [bajt])

Byte = **8 bitů**. Proč 8?

V minulosti existovaly i jiné alternativy, někde byl bajt 7, někde 6, někde 12, někde dokonce 48. Vycházelo to hlavně ze šířky instrukce, kterou podporovaly staré procesory a libovolně velké skupině bytů se říkalo „syllable“ (anglicky „slabika“) než se ustálil pojem „bajt“.

Moderní procesory pracují se 64-bitovými (ale i většími) instrukcemi ale **8 bitový bajt** je standard, který historicky zvítězil a žádné jiné velikosti bajtu se už nepoužívají.

## kilobajt, megabajt, gigabajt…

⚠️ **Důležité k zapamatování**: Historicky se neustálilo jen jedno pravidlo tak se bohužel dodnes používá více způsobů. 

### kilobajt = 1024 bajtů

„Kilo“ znamená 1000, stejně jako „kilometr“ znamená 1000 metrů.

Jenže jak víte, v počítačích je všechno v mocninách čísla 2. Nebylo by tedy lepší, kdyby kilobajt byl 2<sup>10</sup> = 1024? Megabajt by byl 1024 kilobajtů a tak dále. Hezky to do sebe matematicky zapadá, jak jsou to ty mocniny dvou, jiný důvod to nemá.

A proto velmi častý způsob vyjádření množství dat je dle násobitele 1024. Tuto logiku používá operační systém Windows.

- kilobajt (kB) = 2<sup>10</sup> bajtů = 1024 bajtů
- megabajt (MB) = 2<sup>10</sup> kilobajtů = 1024 kilobajtů
- gigabajt (GB) = 2<sup>10</sup> megabajtů = 1024 megabajtů
- atd.

### kilobajt = 1000 bajtů

Ne každý s touto logikou souhlasí a proto se velmi často jednotky počítají i „desítkově“.

- kilobajt (kB) = 1000 bajtů
- megabajt (MB) = 1000 kilobajtů
- gigabajt (GB) = 1000 megabajtů

### „kibibajt“ = 1000 bajtů

Do toho mezinárodní instituce (ISO) zakřičela, že správně je „kilobajt = 1000 bajtů“ a pokud používáte násobky 1024, musíte ve druhé slabice používat „bi“.

- ki**bi**bajt (kiB) = 1024 bajtů
- me**bi**bajt (MiB) = 1024 kibibajtů
- gi**bi**bajt (GiB) = 1024 mebibajtů

Jenže se to vůbec neujalo. Nikdo to nepoužívá a většinou ani nezná. Nikdy jsem nikoho neslyšel mluvit o *kibi*, *mebi* nebo *gibi*bajtech a zaručuji vám, že pokud budete před profesionálem z IT říkat, že *jeden mebibajt má 1024 kibibajtů* tak na vás bude koukat jak na idiota. Je dobré o tom vědět protože tu a tam narazíte na zkratku *kiB* nebo *MiB*.

### kilobit = 1000 bitů

Další velmi často používaný zápis je přímo nad bity, ne nad bajty. Bity a bajty se rozlišují velikostí písmena ale málokdo to používá správně.

MB = mega**bajt**
Mb = mega**bit**

S tímto zápisem se nejčastěji potkáte kdekoliv, kde se měří rychlost, kterou proudí data (např. rychlost zápisu, rychlost čtení, atd.) zejména v počítačových sítích.

Internetový provideři rádi slibují 100MB internet až do domu, jenže těch 100MB není 100 megabajtů ale 100 megabitů — tzn. 100Mb = 100 milionů bitů.

To je úplně jiná hodnota.

- 1 kilobit = 1000 bitů
- 1 megabit = 1000 kilobitů
- 100 megabitů = 100000 kilobitů = 12500000 bajtů (100000000/8)
  - = 11,92 megabajtů (nebo 12,5 mibibajtů)
