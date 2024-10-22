---
draft: false
title: Linuxové distribuce
weight: 100500
---

{{< figure align=center width=100 src="../linux.png" title="Linux logo" >}}

## Linux kernel

Běžný ajťák by měl vědět, že samotný název **Linux** je jen slovo nebo značka která zahrnuje větší množství věcí. 

Co reálně existuje je **Linux kernel** tedy jádro operačního systému Linux, které samo o sobě nic nedělá. [^k]

Toto jádro je **zcela zdarma i pro použití a úpravu na komerční účely** a jeho původní autor Linus Torvalds a celá komunita dalších ajťáků na Linuxovém jádře pracují dodnes.

## Linuxové distribuce

Z tohoto jádra vznikají **konkrétní Linuxové distribuce** což už jsou konkrétní OS, kterých je obrovské množství. Toto se ještě zesložiťuje tím, že některé distribuce jsou postavené na jiných distribucích.

Konkrétně nejznámější Linuxová distribuce **Ubuntu** je postavena na distribuci **Debian**. Mezi další známé distribuce patří **Fedora**, **CentOS**, **Red Hat Enterprise Linux (RHEL)**, **Alpine**. 

Každá tato distribuce má za sebou svoji vlastní skupinu lidí nebo společnost, která tento OS staví a spravuje. Linuxové jádro v každé distribuci může být i libovolně upraveno, reálně tedy **NELZE** říct, že každá Linuxová distribuce má naprosto totožné jádro. Z toho plyne, že program běžící na jedné Linuxové distribuci **nemusí** běžet i na jiné Linuxové distribuci.

<div class="note-blue">

⚠️ **Důležité k zapamatování**: Dvě různé Linuxové distribuce jsou reálně dva různé operační systémy.

</div>

{{< figure align=center width=500 src="../linux-distros.png" title="Linuxové jádro a distribuce" >}}

Linuxovou distribucí je mimochodem i **Android** [^a] o kterém budu mluvit v následujících dílech.

## Pohled do historie: Unix

Důležitý pohled do historie: Linux je inspirován OS zvaným **Unix**. Tento operační systém v nějakých distribucích (např. FreeBSD) existuje dodnes, já jej nepovažuji za běžný OS, se kterým se běžný ajťák (aspoň v českém prostředí) setkává. 

Z Unixu byl postaven i **macOS**. 

Proto je možné při práci s Linuxovými distribucemi a macOS narazit na určité podobnosti - obojí totiž vychází z Unixu.

[^k]: *[StackOverflow - Is it possible to install the Linux kernel alone?](https://unix.stackexchange.com/questions/17122/is-it-possible-to-install-the-linux-kernel-alone)*

[^a]: *Přesto se však Android normálně za samostatnou distribuci nepovažuje. Google má Androida pevně pod kontrolou, vzhledem k zaměření na telefony oproti tradičním distribucím funguje hodně odlišně.*
