---
draft: false
title: Izolace procesu
weight: 210700
---

Každý běžící proces má ve virtuální paměti svůj vlastní přidělený "píseček".

{{< figure align=center width=500 src="../procesy.png" title="Procesy" >}}

<div class="note-blue">

⚠️ **Důležité k zapamatování**: OS nedovoluje procesům jakoukoliv manipulaci s pamětí jiných procesů. Pokud se o to jakýkoliv proces pokusí tak je operačním systémem ukončen. Přístup do paměti jiného procesu se považuje za chybující chování.

</div>