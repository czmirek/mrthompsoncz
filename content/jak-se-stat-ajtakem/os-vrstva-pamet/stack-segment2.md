---
draft: false
title: Stack segment
weight: 213000
---

Zde je shrnutí, co vše stack segment obsahuje.

- Každé vlákno obsahuje **call stack** = kus virtuální paměti dedikovaný pro celé vlákno
- Call stack obsahuje **stack frame** = kus virtuální paměti dedikovaný pro konkrétní volání nějaké podrutiny
- Stack frame jsou naskládané ve struktuře **LIFO** podle toho, jak se řetězí volání jednotlivých podrutin. 
- Pro každé volání podrutiny (podle volací konvence) vzniká nový stack frame.
- Jakmile je podrutina dokončena, stack frame zanikne.

{{< figure align=center width=600 src="../stack-segment.png" title="Stack segment struktura" >}}