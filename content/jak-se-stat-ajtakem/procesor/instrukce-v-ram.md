---
draft: false
title: Schopnost změny instrukce
weight: 70750
---

Z předchozích dílů už víte, že procesor přijímá instrukce z RAM paměti.

Zároveň víte, že procesor je těmito instrukcemi schopný manipulovat data v RAM paměti.

{{< figure align=center width=200 src="../tok.png" title="Interakce procesoru a RAM paměti" >}}

Z toho plyne celkem zjevná věc - **aplikace psaná na bitové vrstvě dokáže za běhu číst data o svých instrukcích a zároveň instrukce za běhu měnit**.