---
draft: false
title: Adresovatelnost
weight: 712
---

Představme si, že během provozu počítače jsou nějaké bity uloženy v RAM paměti a v různých perzistentních komponentách.

{{< figure align=center width=500 src="../nejake-bity.png" title="Nějaké bity" >}}

Jakým způsobem je procesor schopný přesunout **jen některé** bity z RAM na nějaké persistentní uložiště?

RAM paměť je **adresovatelná** což znamená, že všechny bity v RAM jsou rozdělené do nějakých kousků [^k] a každý tento kousek má svoji vlastní **adresu**.

Tato adresa je obyčejné číslo které začíná od 1 pro každý kousek paměti.

{{< figure align=center width=200 src="../adresa.png" title="Bitové adresy" >}}

## RAM = Random Access Memory

RAM paměť má svůj název "RAM" právě díky tomu, že je její obsah je **fyzicky adresovatelný**. Ke každému kousku paměti vedou na základě této adresy **fyzické obvody**. 

Zkratka "RAM" znamená *Random Access*. To znamená, že se k jakémukoliv náhodnému kousku paměti (*random = náhodný*) dostaneme stejně rychle, jako k jakémukoliv jinému náhodnému kousku paměti. [^s]

[^k]: Velikost těchto kousků není stejná a může být mezi jedním a více bajty.
[^s]: RAM paměti v moderních počítačích nejsou zdaleka jedinými zařízeními které umožňují *náhodný přístup ve stejném čase*. Tuto definici splňují i moderní SSD uložiště.    