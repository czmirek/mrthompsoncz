---
draft: false
title: Data segment
weight: 210900
---

Datový segment má **fixní délku** a obsahuje hodnoty, které jsou předem nadefinované již v aplikaci. 

Samotné hodnoty také mají **fixní délku**.

{{< figure align=center width=600 src="../data-segment.png" title="Segmenty procesové paměti" >}}

Proces z těchto hodnot může libovolně **číst i zapisovat** ale **nemůže mazat/přidávat nové hodnoty**.

## Příklad

Jaké hodnoty najdete v datovém segmentu nějaké běžné aplikace? Z pravidla takové, které musí být k dispozici pro celý proces, ne jen pro jednu funkci.

- Například **konfigurace** aplikace. Taková konfigurace může mít vliv na všechny části procesu, proto musí být přístupná všude.
- Dalším příkladem jsou **texty** [^t]. Běžně například texty v horním menu aplikace jako na obrázku níže: "Soubor", "Domů", "Vložení", atd. Tyto názvy se aplikaci často opakují.

{{< figure align=center width=300 src="../word.png" title="Texty aplikace" >}}

[^t]: *Texty mají někdy svůj vlastní segment, to je ale pro běžného ajťáka nepodstatný rozdíl*