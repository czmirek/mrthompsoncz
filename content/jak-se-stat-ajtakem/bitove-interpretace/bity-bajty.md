---
draft: false
title: Bajty
weight: 7020
description: Co je to bajt a jaké jsou další měrné jednotky nad bity i bajty
---

Bajty, kilobajty, gigabajty, atd. jsou měrnou jednotkou bitů stejně jako centimetry, metry a kilometry jsou měrnou jednotkou vzdálenosti.

## byte (čti: [bajt])

<div class="note-blue">

⚠️ byte = **8 bitů**

</div>

Proč 8? Proč vůbec bajt vzniknul? 

Historické důvody. V prastarých počítačích v 50./60. letech v USA vznikla potřeba seskupovat bity do skupin stejné velikosti. Aby se to nepletlo s "bit"-em tak to pojmenovali jako "byte".

První bajty měly 4 bity, někdy 6, někdy 12, někdy dokonce 48 bitů. **8 bitový bajt** je standard, který historicky zvítězil a žádné jiné velikosti bajtu se už nepoužívají.

## kilobajt, megabajt, gigabajt…

<div class="note-blue">

⚠️ **Důležité k zapamatování**: Historicky se neustálilo jen jedno pravidlo pro měření bitů/bajtů tak se bohužel dodnes používá více způsobů. 

</div>

### kilobajt = 1024 bajtů

„Kilo“ znamená 1000, stejně jako „kilometr“ znamená 1000 metrů.

Jenže jak víte, v počítačích je všechno v mocninách čísla 2. Nebylo by tedy lepší, kdyby kilobajt byl 2<sup>10</sup> = 1024? Megabajt by byl 1024 kilobajtů a tak dále. Hezky to do sebe matematicky zapadá, jiný důvod to nemá.

Tuto logiku používá operační systém Windows a spousta jiného softwaru.

- kilobajt (kB) = 2<sup>10</sup> bajtů = 1024 bajtů
- megabajt (MB) = 2<sup>10</sup> kilobajtů = 1024 kilobajtů
- gigabajt (GB) = 2<sup>10</sup> megabajtů = 1024 megabajtů
- atd.

### kilobajt = 1000 bajtů

Ne každý s touto logikou souhlasí a proto se velmi často jednotky počítají i desítkově.

- kilobajt (kB) = 1000 bajtů
- megabajt (MB) = 1000 kilobajtů
- gigabajt (GB) = 1000 megabajtů

### kibibajt = 1000 bajtů

[Mezinárodní organizace pro normalizaci (ISO)](https://cs.wikipedia.org/wiki/Mezin%C3%A1rodn%C3%AD_organizace_pro_normalizaci) přišla s tím, že správně je „kilobajt = 1000 bajtů“ a pokud používáte násobky 1024, musíte ve druhé slabice používat „bi“.

- ki**bi**bajt (kiB) = 1024 bajtů
- me**bi**bajt (MiB) = 1024 kibibajtů
- gi**bi**bajt (GiB) = 1024 mebibajtů

Jenže se to prakticky vůbec neujalo. Nikdo to nepoužívá a většinou ani nezná. Nikdy jsem nikoho neslyšel mluvit o *kibi*, *mebi* nebo *gibi*bajtech a zaručuji vám, že pokud budete před profesionálem z IT říkat, že *jeden mebibajt má 1024 kibibajtů* tak na vás bude koukat jak na idiota.

Je dobré o tom vědět protože tu a tam narazíte na zkratku *kiB* nebo *MiB*.

### kilobit = 1000 bitů

Další velmi často používaný zápis je přímo nad bity. 

<div class="note-blue">

Bity a bajty se rozlišují velikostí písmena ("B" nebo "b") ale ani profesionálové z IT to nepoužívají správně.

- MB = mega**bajt**
- Mb = mega**bit**

</div>

S tímto zápisem se nejčastěji potkáte kdekoliv, kde se měří rychlost, kterou proudí data např. rychlost zápisu, rychlost čtení, atd. Nejčastěji v počítačových sítích.

- 1 kilobit = 1000 bitů
- 1 megabit = 1000 kilobitů
- 100 megabitů = 100000 kilobitů = 12500000 bajtů (100000000/8)
  - = 11,92 megabajtů (nebo 12,5 mibibajtů)
