---
draft: false
title: Frekvence a časování
weight: 402
---

Řekněme pro jednoduchost, že komponenty spolu komunikují morseovkou[^m]. Elektronická komponenta 1 (EL1) chce odeslat elektronické komponentě 2 (EL2) pozdrav "AHOJ" který je v morseovce `.- .... ---. ---`

EL1 začne vysílat první písmeno "A" tedy `.-`

{{< figure align=center width=500 src="../a.png" title="Co odešle EL1" >}}

Jenže EL2 nevidí písmeno "A" ale písmeno "E".

{{< figure align=center width=500 src="../e.png" title="Co vidí EL2" >}}

Jak je to možné?

## Frekvence

Různé počítačové komponenty pracují s informacemi různě rychle.

Komponenta EL1 dokáže odesílat a přijímat zprávy rychlostí 1 signál (krátký nebo dlouhý) za 20 milivteřin. To je jinými slovy frekvence *50 hertzů* (50 Hz) tedy 50 operací za vteřinu.

Komponenta EL2 však signály odesílá a přijímá rychlostí 1 signál za 50 milivteřin tedy 20 Hz. 

EL1 a EL2 se v tomto případě nemohou dorozumět.

{{< figure align=center width=500 src="../timing.png" title="Časování" >}}

## Společný časovač

Řešením tohoto problému je společný časovač který dvěma a více různým komponentám sděluje délku signálu na které budou fungovat. Rychlejší komponenta se musí přizpůsobit pomalejší komponentě.

V moderních počítačích je situace složitější. Moderní počítače obsahují více než jeden časovač (tyto časovače mají zároveň vzájemný matematický vztah), to už je však dle mého názoru nad rámec toho, co potřebuje běžný ajťák o počítačích vědět.

## Vnitřní hodiny

Jiným názvem pro toto *časování* v komponentách je pojem *vnitřní hodiny* nebo v angličtině *clock*[^o]. 

[^m]: V počítačích se morseovka nepoužívá. Morseovku zde zmiňuji pro jednodušší vysvětlení konceptů v signální vrstvy.

[^o]: *Overclocking* je pak manuální zvýšení těchto vnitřních hodin.