---
draft: false
title: Segmenty
weight: 210800
---

Proces se ve virtuální paměti dělí na následující části [^s] kterým se říká **segmenty**.

{{< figure align=center width=200 src="../segmenty.png" title="Segmenty procesové paměti" >}}

- **Code segment**: Instrukce programu. Tato část je pouze pro čtení a má fixní délku. Proces nemůže za běhu měnit své vlastní instrukce.
- **Data segment**: *"pevně nastavená"* paměť
- **Stack**: *"podrutinová"* paměť.
- **Heap**: *"dynamická"* paměť.
- **Volná paměť**

**Data segment**, **stack** a **heap** části podrobně popíšu v následujících kapitolách.

[^s]: *Napříč různými OS může být členění bohatší o nějaké různé, specializované segmenty navíc. To už však není pro běžného ajťáka důležité.*