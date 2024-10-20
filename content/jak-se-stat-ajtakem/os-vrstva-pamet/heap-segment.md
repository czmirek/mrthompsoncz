---
draft: false
title: Heap segment
weight: 214000
---

**Heap segment** nebo jen **heap** je kus virtuální paměti, který se chová jako *data segment* s tím rozdílem, že proces si do **heapu** může za běhu libovolně přidávat a zase z něj odstraňovat cokoliv, co potřebuje.

## Získání paměti

Funguje to následovně:

- proces si řekne OS o kus virtuální paměti s nějakým rozsahem, např. **4 bajty**
- OS ve virtuální paměti najde 4 bajty a předá procesu **adresu virtuální paměti** na tyto 4 bajty

Proces může díky této adrese libovolně číst a měnit jakékoliv bity v tomto 4 bajtovém rozsahu.

{{< figure align=center width=600 src="../heap1.png" title="Heap: vyžádání virtuální paměti" >}}
