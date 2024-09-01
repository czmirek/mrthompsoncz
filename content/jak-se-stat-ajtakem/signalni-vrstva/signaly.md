---
draft: false
title: Signály v IT
weight: 403
---

## Dvoustavový signál

V počítačích se pro odesílání signálu z jednoho místa do druhého používá velmi prostý způsob.

{{< figure align=center width=500 src="../jeneninapeti.png" title="Odeslání signálu v PC" >}}

Toto je nejjednodušší a zároveň **nejlevnější** způsob, jak vyrobit počítačovou komponentu. Rozlišují se pouze dva stavy podle toho, zdali v obvodu je nebo není napětí[^n][^n2]

Je klidně možné postavit komponentu či obvody které rozlišují více než dva stavy (jako v příkladu morseovky v předchozím díle). Problém je v tom, že postavit komponentu která například pracuje se třemi stavy je **mnohonásobně obtížnější** takže i **podstatně dražší** --- takové zařízení zároveň nebude rychlejší.

## Vícestavový signál

V některých případech lze v IT technologiích nalézt vícestavový signál, konkrétně například v některých typech flash pamětí používaných např. v SSD discích.

Tyto flash paměti obsahují buňky, které v sobě jsou schopny uchovat elektrický náboj ve více, než dvou stavech.

## Modulace

...


[^n]: Konkrétní výše napětí ve voltech není pro běžného ajťáka podstatná a může se lišit napříč komponentami ale i napříč různými obvody.

[^n2]: V některých obvodech může být nějaké napětí i ve *spodním stavu* tedy ve stavu, který je na obrázku výše označen jako *Není napětí*. *Horní stav* je pak jen napětí o něco vyšší než ve spodním stavu. 