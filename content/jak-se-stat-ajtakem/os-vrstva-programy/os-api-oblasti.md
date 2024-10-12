---
draft: false
title: OS API / syscalls oblasti
weight: 201500
---

Programy běžící pod OS pro svůj provoz běžně potřebují:

- pracovat s daty v paměti
- ukládat data na persistentní uložiště
- komunikovat po síti/internetu

OS nedovoluje komunikovat s komponentami napřímo. Programy místo toho musí využít **funkce OS** které lze rozdělit na 3 kategorie.

- **Virtuální paměť** = práce s pamětí
- **Souborový systém** = práce s persistentním [^p] uložištěm
- **Síťový interface** = komunikace se sítí/internetem


{{< figure align=center src="../osapioblasti.png" width=600 title="Oblasti OS API / syscalls" >}}


Tyto oblasti si však zaslouží rozepsat v samostatných sekcích.


[^p]: *Souborový systém lze v běžných OS postavit i nad RAM pamětí. Vzhledem k charakteru RAM paměti se po vypnutí počítače všechny soubory z daného souborového uložiště ztratí.*