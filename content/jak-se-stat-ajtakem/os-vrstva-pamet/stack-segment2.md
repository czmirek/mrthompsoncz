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

<div class="note-blue">

⚠️ **Důležité k zapamatování**: Stack segmentu se běžně říká jen **stack**.

</div>

## 🐛 Stack overflow

**Call stack** je flexibilní struktura. Může obsahovat libovolné množství stack framů **ale jen až do určitého limitu** [^s]. Jakmile je tento limit překročen, dojde k chybě a OS proces ukončí.

Ke stack overflow běžně dochází, když si autor nějakého programu nevšimne, že se jeho proces dostává do **nekonečné smyčky** při volání funkcí/podrutin.

- Aplikační kód zavolá funkci A = nový stack frame
- Funkce A zavolá funkci B = nový stack frame
- Funkce B zavolá funkci C = nový stack frame
- Funkce C zavolá funkci A = nový stack frame
- Funkce A zavolá funkci B = nový stack frame
- Funkce B zavolá funkci C = nový stack frame
- Funkce C zavolá funkci A = nový stack frame
- Funkce A zavolá funkci B = nový stack frame
- Funkce B zavolá funkci C = nový stack frame
- atd...

[^s]: *Tento limit je určený kapacitou specializovaného "stack registru" přímo v procesorech.*