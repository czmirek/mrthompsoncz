---
draft: false
title: BIOS a UEFI
weight: 70730
description: Počítač v počítači
---

Základní desky u moderních počítačů obsahují přímo v sobě zabudovaný miniaturní a velmi primitivní "operační systém" kterému se říká **UEFI** nebo u starších počítačů **BIOS**. Nedá se mluvit o plnohodnotném operačním systému, nelze v něm instalovat a spouštět jiné programy.

Pro běžného ajťáka je důležité vědět, že tento systém přebírá roli **bootloaderu** jež se běžně stará o nalezení instrukcí, které má procesor spustit. Ze zapojených dostupných komponent (zpravidla z persistentního uložiště jako SSD, HDD, Flash) se snaží najít tzv. **boot record** což jsou instrukce identifikující začátek nějakého programu.

## UEFI

UEFI je novější standard ve všech moderních počítačích. UEFI je program stejně jako BIOS avšak je na procesoru nezávislý. Běží na samostatném, velmi jednoduchém "mini-procesoru" který je pro UEFI zabudovaný přímo v základní desce. V tomto mini-procesoru je i flash paměť, ve které je UEFI program předpřipravený.

UEFI poznáte tak, že je často graficky mnohem bohatší a oproti BIOSu lze můžete pohybovat i kurzorem myši.

{{< figure align=center width=500 src="../uefi.gif" title="UEFI" >}}

## BIOS

BIOS je v dnešní době už jen ve starších počítačích. Jedná se o program napevno nainstalovaný ve flash paměti jež je napevno zabudovaná přímo v základní desce.

Za spuštění tohoto programu je zodpovědný přímo procesor což znamená, že:

- bez procesoru nelze BIOS spustit
- pro vystoupení z BIOSu je nutné počítač restartovat

BIOS poznáte tak, že je většinou graficky velmi primitivní. Pouze text, rámečky a jednoduché kontrastní barvy. S BIOSem většinou funguje jen klávesnice, nemáte zde kurzor myši.

{{< figure align=center width=500 src="../bios.webp" title="BIOS" >}}