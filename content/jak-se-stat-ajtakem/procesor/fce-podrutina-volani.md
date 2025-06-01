---
draft: false
title: Anatomie volání funkce/podrutiny
weight: 70333.1
---

**Volání funkce** je **konkrétní použití funkce** s **konkrétními dosazenými hodnotami** (pokud jsou nějaké).

Pro vysvětlení anatomie **volání** funkce/podrutiny použiju příklad `7 = SEČTI(3, 4)` z minulé kapitoly.

{{< figure align=center width=500 src="../fxcall.png" title="Volání funkce" >}}

## Vstupní hodnoty

V příkladu SEČTI to jsou hodnoty 3 a 4.

Také lze říct, že:
- *3 je hodnota parametru "sčítanec1"*
- *4 je hodnota parametru "sčítanec2"*

## Vrácená hodnota

V příkladu SEČTI to je hodnota 7. Také lze říct, že *funkce SEČTI vrátila 7*.

## Tělo funkce

Toto jsou konkrétní procesorové instrukce vedoucí ke splnění operace. Pro jednoduché matematické operace jako je sčítání čísel však existují v procesorech již hotové instrukce (`ADD`) a není třeba pro ně psát zvlášť funkce/podrutiny. 