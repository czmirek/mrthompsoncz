---
draft: false
title: Heap segment
weight: 214000
---

**Heap segment** nebo jen **heap** je kus virtuální paměti, který se chová jako *data segment* s tím rozdílem, že proces si do **heapu** může za běhu libovolně přidávat a zase z něj odstraňovat cokoliv, co potřebuje.

## Získání paměti

Funguje to následovně:

- proces si řekne OS o kus virtuální paměti s nějakým rozsahem, např. **4 bajty**
- OS ve virtuální paměti vytvoří 4 bajty
- OS **do aktuálního stack frame** předá **adresu virtuální paměti** na tyto 4 bajty.
- Proces může nyní díky této adrese ze 4 bajtové paměti libovolně číst a libovolně do ní zapisovat 

{{< figure align=center width=700 src="../heap.png" title="Heap: vyžádání virtuální paměti" >}}

<div class="note-blue">

⚠️ **Důležité k zapamatování**: Proces může skrz tuto adresu může libovolně číst a měnit jakékoliv bity v tomto 4 bajtovém rozsahu **a to ze všech vláken po celou dobu běhu procesu** nebo dokud se nerozhodne paměť vrátit (viz. níže).

</div>

## Vrácení paměti

Vrácení paměti je přímočaré.

- Proces sdělí OS API, že už danou položku heapu nepotřebuje a předá adresu, kterou původně od OS API dostal.
- OS API položku uvolní.
- Proces již nemůže adresu jakkoliv využít

<div class="note-blue">

⚠️ **Důležité k zapamatování**: Adresy dodané OS jsou **jediný možný způsob** jak se proces k přidělené paměti může dostat. Pokud špatně naprogramovaný proces adresu ztratí **tak už se k získané paměti nedostane**. 

</div>

<div class="note-blue">

☝️ Jakmile podrutina skončí tak skončí i daný stack frame a s ním i adresa na paměť v heapu. Co proces musí udělat, aby daná paměť byla přístupná i pro další podrutiny?

✅ Proces má dvě možnosti. Může:

- uložit adresu do nějaké připravené položky v **data segmentu**
- adresu vrátit jako **výstupní parametr** funkce/podrutiny

</div>