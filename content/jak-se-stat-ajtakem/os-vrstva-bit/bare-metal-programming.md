---
draft: false
title: Bare-metal programming
weight: 90010
---

V kapitole [Program]({{< relref "../procesor/program" >}}) jsem řekl, že každý software je jen seznam instrukcí pro procesor v dané [instrukční sadě]({{< relref "../procesor/instrukcni-sada" >}})

{{< figure align=center width=200 src="../../procesor/program.png" title="OS = program = seznam instrukcí" >}}

Operační systém (zkráceně OS) není nic jiného, než **program** tedy seznam instrukcí, které se po spuštění počítače načtou do RAM paměti.

## "Bare-metal" a "normální" program

Každý běžný operační systém je program, který běží **přímo nad procesorem**. Tvorbě programů přímo nad procesorem se říká **bare-metal programming** [^n]

Tento typ tvorby softwaru však není praxe běžných ajťáků [^a] a proto se tu dál o něm zmiňovat nebudu. Běžní ajťáci tvoří programy **nad operačním systémem**.

{{< figure align=center width=700 src="../bm-vs-norm-program.png" title="Bare-metal program a normální program" >}}

[^n]: *Doslova "programování na holém železe", myšleno na "prázdném" stroji bez OS.*
[^a]: *Bare-metal programming rozhodně není malý pracovní trh. Lidé v této branži programují procesory ovládající chytré domácnosti, alarmy, roboty a podobně. Tento návod ale není na tento typ ajťáků zaměřen.*