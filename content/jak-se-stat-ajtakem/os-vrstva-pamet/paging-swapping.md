---
draft: false
title: 'Paging / swapping'
weight: 216000
---

Stack a heap rostou "proti sobě". Jakmile se potkají, procesu dojde volná paměť.

{{< figure align=center width=200 src="../segmenty.png" title="Segmenty procesové paměti" >}}

Co je přesně všechno se ale počítá jako **volná virtuální paměť procesu** je složitější problém:

- Ve Windows jsou limity na virtuální paměť závislé na instrukční sadě procesoru a na edici OS
- U Linuxu jsou tyto Limity odlišné v každé distribuci. Některé OS limity nemají žádné (Ubuntu).

---

⚠️ Nezapomeňte, že virtuální pamět umí využívat i **persistentní uložiště** ale k tomu dochází až po té, co dojde fyzciká RAM paměť.

Jakmile dojde fyzická RAM paměť tak OS začnou hekticky přeskládávat kusy paměti mezi RAM a persistentním uložištěm tak. 

- To co *zrovna* nepotřebuje RAM paměť je přesunuto z RAM na disk
- To co *zrovna* potřebuje RAM paměť je přesunuto z disku do RAM

Historicky existují dva způsoby, jak se toto dělá: **paging** a **swapping**. V češtině se často říká **swapování** bez ohledu na skutečný mechanismus, běžného ajťáka normálně nezajímá, jestli daný OS dělá paging, swapping nebo nějaký mix obojího.

<div class="note-blue">

⚠️ **Důležité k zapamatování**: Jakmile OS dojde fyzická RAM paměť tak začne **swapovat** a to není nikdy žádoucí stav. Přesuny z RAM na jakékoliv disky a nazpátek jsou zpravidla **extrémně pomalé**. Swapování ve výsledku vede k obrovskému zpomalení celého systému.

</div>