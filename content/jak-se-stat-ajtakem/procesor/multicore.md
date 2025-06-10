---
draft: false
title: Multijádrové procesory
weight: 70034.1
description: Technologický vývoj a s ním spojené neustálé zmenšování obvodů a tranzistorů v procesoru umožnil, že procesory mají více jader.
---

Procesor zpracovává instrukce v sérii za sebou, jednu po druhé. Technologický vývoj a s ním spojené neustálé zmenšování obvodů a tranzistorů v procesoru však umožnil, že procesory **mají více jader**. 

Jinými slovy, jeden fyzický procesor je ve skutečnosti **několik procesorů** najednou a každý tento procesor dokáže běžet nezávisle na ostatních.

{{< figure align=center width=400 src="../multicore.png" title="Vícejádrový procesor" >}}

## Instrukce u vícejádrových procesorů

<div class="note-blue">

U moderních vícejádrových procesorů se jakýkoliv program spouští vždy **v prvním jádře.** Pokud chce program využít i ostatní jádra, musí k tomu využít specializované instrukce.

</div>

Multijádrové procesory existují až od roku 2001 a do té doby byl veškerý software psán pro obyčejné, "jednojádrové" procesory. Vícejádrový procesor se tedy musí umět chovat tak, jako kdyby byl jednojádrový. Starý program psaný pro jednojádrové procesory poběží na prvním jádře bez jakéhokoliv využití ostatních jader. 