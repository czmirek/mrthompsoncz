---
draft: false
title: Adresovatelnost
weight: 70120
---

Představme si, že během provozu počítače jsou nějaké bity uloženy v RAM paměti a v různých perzistentních komponentách.

{{< figure align=center width=500 src="../nejake-bity.png" title="Nějaké bity" >}}

RAM paměť ale i běžná perzistentní uložiště jsou **adresovatelná** zařízení. To znamená, že všechny bity jsou rozdělené do nějakých kousků [^k] a každý tento kousek má svoji vlastní **adresu**.

Tato adresa je obyčejné číslo.

{{< figure align=center width=200 src="../adresa.png" title="Bitové adresy" >}}

Pro vyjádření adresy v paměti se v praxi používá hexadecimální vyjádření. (příklad: `0x00000FF`).

## RAM = Random Access Memory

RAM paměť má svůj název "RAM" právě díky tomu, že je její obsah je **fyzicky adresovatelný**. Ke každému kousku paměti vedou na základě této adresy **fyzické obvody**. 

Zkratka "RAM" znamená *Random Access*. To znamená, že se k jakémukoliv náhodnému kousku paměti (*random = náhodný*) dostaneme stejně rychle, jako k jakémukoliv jinému náhodnému kousku paměti. [^s]

[^k]: *Velikost těchto kousků není stejná a může být mezi jedním a více bajty.*
[^s]: *RAM paměti v moderních počítačích nejsou zdaleka jedinými zařízeními které umožňují *náhodný přístup ve stejném čase*. Tuto definici splňují i moderní SSD uložiště, přesto se pojem RAM ustálil pouze v kontextu RAM pamětí.*  