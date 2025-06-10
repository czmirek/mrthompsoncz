---
draft: false
title: Synchronní I/O instrukce
weight: 70710
description: Přímá komunikace mezi procesorem a komponentou
---

Procesor teoreticky dokáže komunikovat s každou komponentou **napřímo**. 

- Procesor v instrukci vyšle signál k zařízení **a čeká na odpověď od zařízení** než bude pokračovat v toku instrukcí.
- Zařízení provede nějakou svoji operaci na základě signálu a vrátí odpověď procesoru
- Procesor obdrží odpověď a **pokračuje v toku instrukcí**.

Tomu se říká synchronní komunikace.

{{< figure align=center width=500 src="../syncio2.png" title="Sybchronní komunikace" >}}

<div class="note-blue">

⚠️ **Důležité k zapamatování:** Procesory běžných počítačů nikdy nekomunikují s ostatními zařízeními synchronně. **Jakékoliv vstupní či výstupní zařízení je řádově pomalejší, než samotný procesor**. Procesor může čekáním vyplýtvat celé miliardy cyklů čekáním na zařízení s rychlostí 100 Hz tedy 100 cyklů za vteřinu.

</div>