---
draft: false
title: Spuštění procesu
weight: 210500
---

Při spuštění programu se instrukce tohoto programu načtou do **user space** virtuální paměti a vznikne [proces]({{< relref "../os-vrstva-programy/proces" >}}).

{{< figure align=center width=500 src="../spusteniprogramu.png" title="Spuštění programu" >}}

<div class="note-blue">

⚠️ **Důležité k zapamatování**: Operační systémy **nedovolují procesům [měnit své vlastní instrukce]({{< relref "../procesor/instrukce-v-ram" >}})**. 

Časem se totiž ukázalo, že běžný software tuto přirozenou schopnost procesoru nevyužívá [^z]. Často to však využívají viry a záškodnické programy, které se tímto způsobem vyhýbají antivirům.

</div>

[^z]: *Z logických důvodů které budou jasné až v kapitolách o tvorbě softwaru.*