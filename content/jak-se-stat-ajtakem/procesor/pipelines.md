---
draft: false
title: CPU pipeline
weight: 704
---

Moderní procesory zpracovávají instrukce v několika krocích a počet těchto kroků je různý napříč různými modely procesorů. Některé procesory mohou potřebovat 10, některé až 50 kroků k vykonání některých instrukcí.

Těmto *postupům* se v angličtině se tomu říká **CPU pipeline**.

{{< figure align=center width=300 src="../pipeline.png" title="Cyklus procesoru" >}}

⚠️ **Důležité k zapamatování**: Mechanismus "CPU pipeline" je odlišný procesor od procesoru. Běžný ajťák nezná a nepotřebuje vědět, jak procesorová pipelina konkrétního procesoru funguje.  