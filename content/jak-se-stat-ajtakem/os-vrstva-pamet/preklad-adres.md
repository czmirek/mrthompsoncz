---
draft: false
title: Překlad adres
weight: 210300
---

V kapitole o RAM paměti jsem řekl, že RAM paměť je [adresovatelná]({{< relref "../procesor/adresy" >}}).

Virtuální paměť je také adresovatelná, jde však o úplně jiné adresy které nekorespondují s fyzickými adresami v RAM paměti. Programy běžící pod OS nemají vůbec k adresám RAM paměti přístup.

OS se tak stará o **překlad adres** mezi virtuální pamětí a RAM pamětí a případně i persistentním uložištěm.

{{< figure align=center width=400 src="../preklad-adres.png" title="Překlad adres" >}}

<div class="note-blue">

⚠️ **Důležité k zapamatování**: toto mapování je pro programy běžící v OS neviditelné. Žádný program v OS neví, zdali se jeho paměť nachází v RAM paměti nebo jestli se zrovna využívá persistentní uložiště.

</div>