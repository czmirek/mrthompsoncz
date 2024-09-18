---
draft: false
title: BIOS a UEFI
weight: 773
---

Základní desky u moderních počítačů obsahují přímo v sobě zabudovaný miniaturní a velmi primitivní "operační systém". Nedá se ale ještě mluvit o plnohodnotném operačním systému. Běžně v něm nelze instalovat a spouštět jiné programy.

Tento systém slouží pro diagnostiku a konfiguraci počítače a jednotlivých komponent na úplně základní úrovni která nemusí být možná v rámci plnohodnotného operačního systému.

Pro běžného ajťáka je důležité vědět, že tento systém se běžně stará o nalezení instrukcí, které má procesor spustit. Tyto instrukce běžně představuje plnohodnotný operační systém.

Existují dva standardy těchto systémů: BIOS a UEFI

## BIOS

BIOS je v dnešní době už jen ve starších počítačích. Jedná se o program napevno nainstalovaný ve flash paměti která je napevno zabudovaná přímo v základní desce.

Za spuštění tohoto programu je zodpovědný přímo procesor což znamená, že:

- bez procesoru nelze BIOS spustit
- pro vystoupení z BIOSu je nutné počítač restartovat

BIOS poznáte tak, že je většinou graficky velmi primitivní. Pouze text, rámečky a jednoduché kontrastní barvy. S BIOSem většinou funguje jen klávesnice, nemáte zde kurzor myši.

{{< figure align=center width=500 src="../bios.webp" title="BIOS" >}}

## UEFI

UEFI je novější standard ve všech moderních počítačích. UEFI je program stejně jako BIOS avšak je na procesoru nezávislý. Běží na samostatném čipu nebo na velmi jednoduchém "mini-procesoru" který je pro UEFI zabudovaný přímo v základní desce. V tomto mini-procesoru je i flash paměť, ve které je UEFI program uložený.

UEFI poznáte tak, že je často graficky mnohem bohatší a můžete zde pohybovat i s kurzorem myši.

{{< figure align=center width=500 src="../uefi.gif" title="UEFI" >}}
