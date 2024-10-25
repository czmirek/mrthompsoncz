---
draft: false
title: 🐛 Memory leak
weight: 215100
---

Situaci, kdy proces nevrátí již nepoužívanou paměť, se říká **memory leak** a toto se považuje za chybné chování programu. Procesy by měly nepoužitou paměť vracet, jakmile ji nepotřebují.

<div class="note-blue">

⚠️ **Důležité k zapamatování**: Adresy na virtuální paměť, kterou proces získal od OS jsou **jediný možný způsob** jak se proces k přidělené paměti může dostat. 

Pokud špatně naprogramovaný proces adresu ztratí **tak už se k získané paměti nedostane** a tudíž ji nemůže ani vrátit tzn. došlo k memory leaku.

</div>

