---
draft: false
title: "Heap segment: vrácení paměti"
weight: 215000
---

Vrácení paměti je přímočaré.

- Proces sdělí OS API, že už danou položku heapu nepotřebuje a předá adresu, kterou původně od OS API dostal.
- OS API položku uvolní.
- Proces již nemůže adresu jakkoliv využít

## 🐛 Memory leak

Situaci, kdy proces nevrátí již nepoužívanou paměť, se říká **memory leak**.

<div class="note-blue">

⚠️ **Důležité k zapamatování**: Adresy na virtuální paměť, kterou proces získal od OS jsou **jediný možný způsob** jak se proces k přidělené paměti může dostat. 

Pokud špatně naprogramovaný proces adresu ztratí **tak už se k získané paměti nedostane** tzn. došlo k memory leaku.

</div>


