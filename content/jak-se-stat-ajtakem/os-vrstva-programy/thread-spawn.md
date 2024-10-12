---
draft: false
title: Thread spawn
weight: 201100
---

Každý program má vždy minimálné **hlavní vlákno**. Konec hlavního vlákna znamená, že končí i celý proces.


<div class="note-blue">

⚠️ **Důležité k zapamatování:** Proces může mít kromě hlavního vlákna ještě libovolné množství dalších vláken. Po skončení hlavního vlákna však OS pozabíjí jakákoliv ostatní vlákna, která si proces vytvořil a které nedoběhly do konce. 

</div>

{{< figure align=center src="../vlakna.png" width=300 title="Proces s pěti běžícími vlákny" >}}