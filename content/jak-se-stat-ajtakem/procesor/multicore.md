---
draft: false
title: Multijádrové procesory
weight: 70500
---

Jak víte z předchozích dílů, procesor zpracovává instrukce v sérii za sebou, jednu po druhé. Přestože moderní procesory obsahují více krokové *pipeliny* které jsou schopné v každém kroku zpracovávat jednu instrukci tak není možné, aby v rámci jednoho kroku pipeliny bylo zpracováváno více, než jedna instrukce.

Technologický vývoj a s ním spojené neustálé zmenšování obvodů a tranzistorů v procesoru však umožnil, že procesory **mají více jader**. 

Jinými slovy, jeden fyzický procesor je ve skutečnosti **několik procesorů** najednou a každý tento procesor dokáže běžet nezávisle na ostatních.

{{< figure align=center width=400 src="../multicore.png" title="Vícejádrový procesor" >}}

## Instrukce u vícejádrových procesorů

Procesor ale nemá žádný názor na to, která instrukce by měla běžet v jakém jádře. Jeho výchozí chování je, že jakékoliv instrukce, které dostane, běží v prvním jádře.

To je kvůli zpětné kompatibilitě. Multijádrové procesory existují až od roku 2001 a do té doby byl veškerý software psán pro obyčejné, "jednojádrové" procesory. Vícejádrový procesor se tedy musí umět chovat tak, jako kdyby byl jednojádrový.

Pokud chcete, aby nějaké instrukce v RAM paměti běžely paralelně v jiném jádře pak je nutné procesor takto instruuovat. Pokud budete mít program nebo operační systém psaný pro starší jednojádrové procesory tak ten program normálně poběží na prvním jádře bez jakéhokoliv využití ostatních jader. 