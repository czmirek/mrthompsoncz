---
draft: false
title: Adresovatelnost
weight: 70090
description: RAM paměť je adresovatelné zařízení.
---

RAM paměť je **adresovatelné** zařízení.

To znamená, že všechny bity jsou rozdělené do nějakých kousků [^k] a každý tento kousek má svoji vlastní zadrátovanou **fyzickou adresu**.

Fyzická adresa je obyčejné číslo, které se v praxi vždy vyjadřuje v hexadecimální formě. (např.: `0x00000FF`).

{{< figure align=center width=500 src="../adresa2.png" title="Bitové adresy" >}}


## RAM = Random Access Memory

RAM paměť má svůj název "RAM" právě díky tomu, že je její obsah je **fyzicky adresovatelný**. Ke každému kousku paměti vedou na základě této adresy **fyzické obvody**. 

Zkratka "RAM" znamená *Random Access Memory*. To znamená, že se k jakémukoliv náhodnému kousku paměti (*random = náhodný*) dostaneme stejně rychle, jako k jakémukoliv jinému náhodnému kousku paměti. [^s]

[^k]: *Velikost 1 kousku je obvykle 1 bajt.*
[^s]: *RAM paměti v moderních počítačích nejsou zdaleka jedinými zařízeními které umožňují *náhodný přístup ve stejném čase*. Tuto definici splňují i moderní SSD uložiště, přesto se pojem RAM ustálil pouze v kontextu RAM pamětí.*  