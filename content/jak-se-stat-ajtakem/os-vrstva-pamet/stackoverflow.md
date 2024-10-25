---
draft: false
title: "🐛 Stack overflow"
weight: 213100
---

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