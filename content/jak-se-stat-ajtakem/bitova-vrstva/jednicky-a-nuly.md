---
draft: false
title: Jedničky a nuly
weight: 601
---

V počítačích informace putují pouze jedním způsobem:

{{< figure align=center width=500 src="../jeneninapeti.png" title="Digitální signál" >}}

Konkrétní výše napětí ve voltech pro stav "*Je napětí*" není pro běžného ajťáka podstatná. Podstatné je to, že jsou možné **pouze dva stavy** a tímto způsobem se předávají v počítači informace.   

Binární (nebo také **digitální**) vrstva je jednoduše kódování, ve kterém říkáme, že:

- Tam, kde je signál (napětí), tam je číslice 1
- Tam, kde není signál (napětí), tam je číslice 0

{{< figure align=center width=500 src="../binmsg.png" title="Příklad nějaké digitální zprávy" >}}

## Proč nejde použít víc úrovní napětí a mít víc, než jen 2 úrovně signálů?

**Ono to jde!** V minulosti se i experimentovalo s elektronickými **třístavovými počítači**. Teoreticky je možné postavit počítače které umí pracovat s libovolným množstvím stavů.

Problém je v tom, že už jenom jeden jediný stav navíc **extrémně zesložiťuje** a tudíž **zdražuje** stavbu jakýchkoliv elektronických komponent. Takový počítač tedy není rozhodně levnější a pravděpodobně ani rychlejší.