---
draft: false
title: Linuxové distribuce
weight: 100500
---

## Linux kernel

Běžný ajťák by měl vědět, že samotný název **Linux** je spíš jen značka. Co reálně existuje je **Linux kernel** tedy jádro operačního systému Linux, které samo o sobě nic nedělá. [^k]

Toto jádro je **zcela zdarma i pro použití a úpravu na komerční účely** a jeho původní autor Linus Torvalds a celá komunita dalších ajťáků na Linuxovém jádře pracují dodnes.

## Linuxové distribuce

Z tohoto jádra vznikají **konkrétní Linuxové distribuce** což už jsou konkrétní OS, kterých je obrovské množství. Dále to komplikuje fakt, že některé distribuce jsou postavené na jiných distribucích.

Konkrétně nejznámější Linuxová distribuce **Ubuntu** je postavena na distribuci **Debian**. Mezi další známé distribuce patří **Fedora**, **CentOS**, **Red Hat Enterprise Linux (RHEL)**, **Alpine**. 

Každá tato distribuce má za sebou svoji vlastní skupinu lidí nebo společnost, která tento OS staví a spravuje. Linuxové jádro v každé distribuci může být i libovolně upraveno, reálně tedy **NELZE** říct, že každá Linuxová distribuce má naprosto totožné jádro. Z toho plyne, že program běžící na jedné Linuxové distribuci **nemusí** běžet i na jiné Linuxové distribuci.

{{< figure align=center width=500 src="../linux-distros.png" title="Linuxové jádro a distribuce" >}}

Linuxovou distribucí je mimochodem i **Android** [^a] o kterém budu mluvit v následujících dílech.

[^k]: *[StackOverflow - Is it possible to install the Linux kernel alone?](https://unix.stackexchange.com/questions/17122/is-it-possible-to-install-the-linux-kernel-alone)*

[^a]: *Přesto se však Android za samostatnou distribuci nepovažuje. Google má Androida pevně pod kontrolou, vzhledem k zaměření na telefony oproti tradičním distribucím funguje hodně odlišně a není moc běžné, že byste Androida někam instalovali.*
