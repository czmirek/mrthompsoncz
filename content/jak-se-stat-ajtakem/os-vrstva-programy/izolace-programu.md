---
draft: false
title: Izolace programu v uživatelském režimu
weight: 201300
---

<div class="note-blue">

⚠️ **Důležité k zapamatování:** V uživatelském režimu běží **všechny** procesy spuštěné v rámci OS. 

</div>

{{< figure align=center src="../izolace2.png" width=600 title="Izolace OS programů" >}}

Jakýkoliv pokus o přímou komunikaci s jakoukoliv komponentou CPU zablokuje a způsobí přerušení které OS zachytí a chybující proces ukončí.