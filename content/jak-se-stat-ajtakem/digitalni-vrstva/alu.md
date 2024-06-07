---
draft: false
title: ALU
weight: 480
---

Tato kapitola je poslední kapitola, ve které vysvětluji, jak procesor pracuje s čísly.

Každý procesor obsahuje část, které se říká ALU – v angličtině „Arithmetic logic unit“, v češtině Aritmeticko-logická jednotka.

Tato část procesoru není nic jiného než kalkulačka, která umí dělat operace s celými čísly ve dvojkovém doplňku a s desetinnými čísly v plovoucí desetinné čárce . (Někdy se části procesoru pracující s desetinnými čísly říká FPU – „floating-point unit“ nebo „jednotka plovoucí desetinné čárky“)

Souhrnně ALU (nebo ALU+FPU) není nic jiného, než kalkulačka, která umí všechny možné matematické operace, které jsou v ní sestavené pomocí hradel nad 32 nebo 64 bitovými hodnotami, ať už jde o celá čísla ve dvojkovém doplňku, nebo o desetinná čísla v IEEE 754.

Zpravidla je to zadrátované tak, že procesor ovládá nějakou sadu matematických instrukcí, jejichž provedení deleguje právě do ALU.

Nezapomeňte na to, že všechny tyto matematické operace okolo dvojkového doplňku a plovoucí desetinné čárky nejsou reálně není nic jiného, než elektřina putující v reálných elektrických obvodech ve fyzické vrstvě!

![ALU](/jak-se-stat-ajtakem/digitalni-vrstva/alu.png)

## Shrnutí

- ALU je část procesoru, která se zabývá veškerými matematickými operacemi s celými a desetinnými čísly (někdy se část pracující s desetinnými čísly označuje jako FPU)