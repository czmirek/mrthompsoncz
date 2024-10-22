---
draft: false
title: Izolace procesu
weight: 210700
---

Každý běžící proces má ve virtuální paměti svůj vlastní přidělený "píseček".

{{< figure align=center width=500 src="../procesy.png" title="Procesy" >}}

<div class="note-blue">

⚠️ **Důležité k zapamatování**: OS nedovoluje procesům jakoukoliv manipulaci s pamětí jiných procesů. Pokud se o to jakýkoliv proces pokusí tak je operačním systémem ukončen. Přístup do paměti jiného procesu se považuje za chybující chování.

</div>

## 🐛 Segmentation fault [^s]

**Segmentation fault** nebo taky jen zkráceně `segfault` je označení pro chybu softwaru, který se snaží přistupovat (číst/zapisovat) paměť, do které nemá přístup.

- buď tato paměť patří jinému procesu
- nebo procesu nebyla vůbec přidělena
- nebo už procesu nepatří

[^s]: *🐛 je emoji pro "bug". Anglické slovo "bug" znamená doslova "brouk" ale v IT se používá pro označení jakékoliv chyby. Mezi profesionálními ajťáky ale i vysokoškolskými profesory je populární historka, že slovo "bug" vzniklo díky jednomu inženýrovi na konci druhé světové války, kterému přestal fungovat počítač [kvůli můře](https://english.stackexchange.com/a/40935) která mu tam vletěla. Použití slova "bug" jako nějaké chyby nebo závady je ale [mnohem starší](https://english.stackexchange.com/a/40936) (~1880).*