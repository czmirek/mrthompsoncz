---
draft: true
title: Hardwarové složitosti které lze ignorovat
weight: 310
---

V kapitole na úvodu jsem pojmenoval Von Neumannovu architekturu, na které jsou všechny moderní počítače více méně postavené.

V moderních počítačích je ale realita mnohem komplikovanější.

Jak už víte, každá komponenta v počítači běží pod určitou rychlostí. Architektura moderního počítače obsahuje obrovské množství různých pomocných obvodů a čipů, nebo "*bufferů*" které slouží právě k dočasnému uložení dat mezi komponentami, které pracují na různých rychlostech.

Samotný procesor obsahuje přímo v sobě sadu různých miniaturních pamětí kterým se říká *cache* která jsou odstupňované od nejrychlejší (L1) po nejpomalejší (až L4) a tyto *cache* mohou být v procesoru vyrobeny i za použití jiné výrobní technologie. Data, se kterými procesor *právě tento okamžik* pracuje se nachází v *registrech*.

Toto dále zesložiťuje fakt, že každý výrobce k tomu může mít jiný přístup.

- Každá základní deska může obsahovat úplně jiné uspořádání čipů/bufferů
- Každá komponenta může obsahovat úplně jiné uspořádání čipů/bufferů
- Každý procesor může obsahovat úplně jiné uspořádání „cache“ a „registrů“

Realita, jak a kudy tečou v moderních počítačích data, by se lépe dala znázornit následujícím obrázkem.


{{< figure align=center src="../hwcmp.png" title="Hardwarové složitosti, které lze ignorovat" >}}


<div class="note-blue">

Pointa této kapitoly je, že to není pro nás ajťáky vůbec důležité!
Tyto složitosti na úrovni hardwaru nejenom, že často neznáme ale ani je pro svoji práci vůbec znát nepotřebujeme. Důležité je pouze chápat Von Neumannův model.

Každý hardware funguje uvnitř dost odlišně už jen proto, že výrobci hardwaru si navzájem konkurují výkonem, spolehlivostí a kompatibilitou.

</div>