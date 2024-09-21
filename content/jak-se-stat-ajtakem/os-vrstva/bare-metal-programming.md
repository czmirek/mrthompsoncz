---
draft: false
title: Bare-metal programming
weight: 90010
---

V kapitole [Program]({{< relref "../procesor/program" >}}) jsem řekl, že každý software je jen seznam instrukcí pro procesor v dané [instrukční sadě]({{< relref "../procesor/instrukcni-sada" >}})

{{< figure align=center width=200 src="../../procesor/program.png" title="OS = program = seznam instrukcí" >}}

Operační systém (zkráceně OS) není nic jiného, než **program** tedy seznam instrukcí, které se po spuštění počítače načtou do RAM paměti.

## Je možné vyrobit svůj vlastní OS?

Samozřejmě že ano! 

Můžete naprogramovat jakoukoliv aplikaci přímo pro procesor. Tomuto programování se říká **bare-metal programming** [^n]. 

Tento typ tvorby softwaru však není praxe běžných ajťáků a proto se tu dál o něm zmiňovat nebudu. Běžní ajťáci pracují nad vrstvou OS tudíž by běžný ajťák měl dobře rozumět, jak OS fungují.

[^n]: *Doslova "programování na holém železe", myšleno na "prázdném" stroji bez OS.*