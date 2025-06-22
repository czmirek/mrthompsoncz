---
draft: false
title: Jedničky a nuly
weight: 601
description: Jak signály v počítači reprezentují pouze dva stavy v podobě jedniček a nul
---

V počítačích putují informace pouze jedním způsobem:

{{< figure align=center width=700 src="../jeneninapeti.png" title="Digitální signál" >}}

Konkrétní výše napětí ve voltech není podstatná. Podstatné je, že jsou možné **pouze dva stavy**.

Binární (nebo také **digitální**) vrstva je jednoduše kódování, ve kterém říkáme, že:

- Tam, kde je signál/napětí/horní stav - tam je číslice 1
- Tam, kde není signál/napětí/spodní stav - tam je číslice 0

{{< figure align=center width=700 src="../binmsg.png" title="Příklad digitální zprávy" >}}

## Proč nejde použít víc úrovní napětí a mít víc, než jen 2 úrovně signálů?

**Ono to jde!** V minulosti se experimentovalo s elektronickými **třístavovými počítači**. Teoreticky je možné postavit počítače které umí pracovat s libovolným množstvím stavů.

Jediný stav navíc **zesložiťuje** a **zdražuje** stavbu elektronických komponent, takový počítač **není rychlejší** a neumí navíc nic, co by binární (dvoustavový) počítač nedokázal. 