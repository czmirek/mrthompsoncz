---
draft: false
title: Hardwarové složitosti které lze ignorovat
weight: 790
---

Každá komponenta v počítači běží pod určitou rychlostí. Architektura moderního počítače obsahuje obrovské množství různých pomocných obvodů a čipů, nebo "*bufferů*" které slouží právě k dočasnému uložení dat mezi komponentami, které pracují na různých rychlostech.

Samotný procesor obsahuje přímo v sobě sadu různých miniaturních pamětí kterým se říká *cache*. Tyto paměti jsou odstupňované od nejrychlejší (L1) po nejpomalejší (až L4) a tyto *cache* mohou být v procesoru vyrobeny i za použití jiné výrobní technologie.

Data, se kterými procesor *právě tento okamžik* pracuje se nachází v *registrech*.

Každý výrobce však k tomu může mít jiný přístup.

- Každá základní deska může obsahovat úplně jiné uspořádání čipů/bufferů
- Každá komponenta může obsahovat úplně jiné uspořádání čipů/bufferů
- Každý procesor může obsahovat úplně jiné uspořádání cache, registrů a odlišné chování pipeline i 

Realita, jak a kudy tečou v moderních počítačích konkrétní bity, by se lépe dala znázornit následujícím obrázkem.


{{< figure align=center src="../hwcmp.png" title="Hardwarové složitosti, které lze ignorovat" >}}


<div class="note-blue">

⚠️ Pointa této kapitoly je, že pro běžného ajťáka není důležité se těmito detaily vůbec zabývat. Tyto složitosti na úrovni hardwaru nejenom, že často neznáme ale ani je pro svoji práci vůbec znát nepotřebujeme. 

Důležité je rozumět jak funguje procesor a jak procesor interaguje se zbytkem počítače.

</div>