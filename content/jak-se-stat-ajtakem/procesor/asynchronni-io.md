---
draft: false
title: Asynchronní I/O instrukce
weight: 70720
description: Nepřímá komunikace mezi procesorem a komponentami
---

Procesor v běžných počítačích komunikuje s ostatními komponentami **nepřímo** neboli **asynchronně**. 

Procesor použije specializované instrukce, kterými nařizuje čipsetu základními desky následující:

- **pro čtení:** připrav data z nějaké komponenty do RAM paměti
- **pro zápis:** vem data z RAM paměti a odešli je do nějaké komponenty

Procesor komanduje základní desku, aby komunikaci s ostatními komponentami obstarala za něj a může pokračovat v běžném toku instrukcí.

Jakmile je operace čtení/zápisu hotová tak chipset základní desky pošle do procesoru **přerušení** na které procesor může navázat.

{{< figure align=center width=500 src="../asyncio.png" title="Asynchronní komunikace" >}}

Tomuto systému se v počítačích říká **DMA** neboli *Direct Memory Access*.