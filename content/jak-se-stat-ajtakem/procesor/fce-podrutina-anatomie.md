---
draft: false
title: Anatomie definice funkce/podrutiny
weight: 70332
---

Pro vysvětlení anatomie **definice** funkce/podrutiny použiju příklad `7 = SEČTI(3, 4)` z minulé kapitoly.

**Definice funkce** je jenom takový lidský zápis díky kterému hned poznáte:

- název funkce
- kolik má vstupních parametrů. Jednotlivé parametry jsou oddělené čárkou
- co je výstupem funkce

{{< figure align=center width=700 src="../fxdef.png" title="Definice funkce" >}}

## Vstupní parametry

Vstupní parametry náleží k definici funkce. V příkladu SEČTI na obrázku výše to jsou **sčítanec1** a **sčítanec2**.

<div class="note-blue">

⚠️ Funkce může mít libovolné množství vstupních parametrů **ale také nemusí mít žádný vstupní parametr**.

Příklady definic:

```
FUNKCE_1()
FUNKCE_2(parametr1)
FUNKCE_3(parametr1, parametr2)
FUNKCE_4(parametr1, parametr2, parametr3)

atd...
```

</div>

## Výstup funkce

Výstup funkce náleží k definici funkce. V příkladu SEČTI na obrázku výše to je **součet**.

<div class="note-blue">

⚠️ **Důležité k zapamatování**: Funkce má buď **přesně jednu** výstupní hodnotu, nebo **žádnou výstupní hodnotu**. Toto ještě jednou zopakuji v příští kapitole v jiném kontextu, kdy to bude jasnější.

Příklady definic:

```
FUNKCE_1() <------------------------------------ nemá výstup
output = FUNKCE_2(parametr1)
output = FUNKCE_3()
output = FUNKCE_4(parametr1, parametr2, parametr3)
FUNKCE_5(parametr1, parametr2, parametr3)   <--- nemá výstup

atd...
```

</div>