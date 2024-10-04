---
draft: false
title: Režimy CPU
weight: 201200
---

- Připomeňme si znovu kapitolu [Sdílená kapacita procesoru]({{< relref "sdilena-kapacita" >}}) kde jsem řekl, že OS sdílí kapacitu procesoru s programy, které pod ním běží.

- Připomeňme si zároveň ještě kapitolu [Schopnost změny instrukce]({{< relref "../procesor/instrukce-v-ram" >}}). Zde píšu, že procesor má schopnost sám sobě měnit instrukce v RAM paměti.

To logicky vede k otázce - **Může program běžící v rámci OS změnit instrukce samotného OS?** To by byl obrovský bezpečnostní problém. Jakýkoliv program by tímto způsobem mohl získat kompletní kontrolu nad vaším počítačem a mohl by ignorovat jakákoliv pravidla která OS nastavuje.

Tento problém je řešený **už na úrovni procesoru** skrz **procesorové režimy**.

## Jak to funguje

Moderní procesory podporují 2 základní režimy [^a] zvané:
- **privilegovaný režim**
- **uživatelský režim**


## Privilegovaný režim
Při zapnutí počítače běží procesor v privilegovaném režimu. V tomto režimu je možné v procesoru spustit jakoukoliv instrukci bez omezení. Díky těmto instrukcím OS komunikuje s komponentami napřímo nebo skrz nějaké zadrátované, hardwarové mechanismy. Na této úrovni pracuje operační systém a jeho instrukce běží v privilegovaném režimu.

## Uživatelský režim
Jakýkoliv proces uvnitř OS však běží v uživatelském režimu. Toto má za následek, že žádný proces v OS **nemůže komunikovat se žádnou komponentou napřímo** [^s]. Jakmile se jakýkoliv proces o toto pokusí tak to OS vyhodnotí jako chybu a proces "zabije". 

{{< figure align=center width=300 src="../rezimy.png" title="Režimy procesoru" >}}

[^a]: *V rámci tohoto návodu se budeme bavit později bavit ještě o třetím, "virtualizačním" režimu*
[^s]: *Situace se trochu komplikuje jakmile se začneme bavit o ovladačích neboli "driverech" ale to teď není důležité.*