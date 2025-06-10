---
draft: false
title: Čipset základní desky
weight: 70600
description: Jak procesor komunikuje s ostatními komponentami
---

Procesor komunikuje s ostatními komponentami skrz **čipset základní desky**. To je sada různých specializovaných čipů a obvodů, jejichž jediným účelem je zprostředkovat komunikaci mezi procesorem a různými **sběrnicemi**.

**Sběrnice** je specializovaný obvod, ke kterému se fyzicky připojuje nějaká komponenta. Existují různé druhy sběrnic. K některým lze připojit téměř jakékoliv zaříení (např. USB) a některé jsou více specializované na druh či konstrukci zařízení (např. PCI, PCIe, SATA).

{{< figure align=center width=700 src="../cipset2.png" title="Komunikace mezi procesorem a ostatními komponentami" >}}

<div class="note-blue">

⚠️ **Důležité k zapamatování:** Obrovské složitosti tvořené všemi možnými mezinárodní korporáty zabývající se IT a výrobou počítačové techniky *(Intel, AMD, NVIDIA, atd.)* je lepší nechat na autorech operačních systémů. Běžný ajťák se těmito tématy (většinou) nezabývá.

</div>