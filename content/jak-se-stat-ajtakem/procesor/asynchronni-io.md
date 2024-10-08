---
draft: false
title: Asynchronní I/O instrukce
weight: 70720
---

Asynchronní I/O instrukce fungují oproti synchronním instrukcím tak, že procesor těmito instrukcemi instruuje chipset základní desky aby:

- **pro čtení:** připravil data která potřebuje do RAM paměti
- **pro zápis:** data z RAM paměti vzal a zapsal je do dané I/O komponenty.

Tímto způsobem procesor komanduje základní desku co má dělat, nemusí se zdržovat čekáním na ostatní komponenty a může pokračovat ve zpracovávání běžného toku instrukcí.

Jakmile je operace čtení/zápisu hotová tak chipset základní desky pošle do procesoru **přerušení** na které procesor může navázat.

{{< figure align=center width=500 src="../asyncio.png" title="Asynchronní komunikace" >}}

Tomuto systému se v počítačích říká **DMA** neboli *Direct Memory Access*.