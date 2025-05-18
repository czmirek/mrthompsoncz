---
draft: false
title: Frekvence a časování
weight: 402
---

Řekněme pro jednoduchost, že komponenty v počítačích spolu komunikují morseovkou [^m].

Elektronická komponenta 1 (EL1) chce odeslat elektronické komponentě 2 (EL2) pozdrav "AHOJ" který je v morseovce `.- .... ---. ---`

EL1 začne vysílat první písmeno "A" tedy `.-`

{{< figure align=center width=500 src="../a.png" title="Co odešle EL1" >}}

Jenže EL2 nevidí písmeno "A" ale písmeno "E".

{{< figure align=center width=500 src="../e.png" title="Co vidí EL2" >}}

Jak je to možné?

## Frekvence

Každá počítačová komponenta pracuje na určité frekvenci. To mimojiné znamená, jak rychle je schopna přijímat a posílat zprávy.

- EL1 = rychlá komponenta - na frekvenci např. 50 Hz pošle/přijme 50 signálů za vteřinu
- EL2 = pomalá komponenta - na frekvenci např. 10 Hz pošle/přijme 10 signálů za vteřinu

EL1 a EL2 se v tomto případě nemohou dorozumět.

{{< figure align=center width=500 src="../timing.png" title="Časování" >}}

## Časovač

Řešením je společný časovač který dvěma a více různým komponentám sděluje délku signálu na které budou fungovat. Rychlejší komponenta se musí přizpůsobit pomalejší komponentě.

Moderní počítače obsahují mnoho časovačů, které mají mezi sebou matematický vztah. Toto už je ale nad rámec znalostí běžného ajťáka.

## Vnitřní hodiny

Jiným názvem pro toto *časování* v komponentách je pojem *vnitřní hodiny* nebo v angličtině *clock* [^o]. 

[^m]: *V počítačích se morseovka nepoužívá. Její použití zde slouží pouze pro výukové účely.*

[^o]: *Overclocking je pak manuální zvýšení těchto vnitřních hodin.*