---
draft: false
title: CPU pipeline
weight: 70040
---

Moderní procesory zpracovávají instrukce v několika krocích a počet těchto kroků je různý napříč různými modely procesorů. Některé procesory mohou potřebovat 10, některé až 50 kroků k vykonání některých instrukcí.

Těmto *postupům* se v angličtině říká **CPU pipeline** (počeštěně "pajplajna").

{{< figure align=center width=300 src="../pipeline.png" title="Cyklus procesoru" >}}

⚠️ **Důležité k zapamatování**: Mechanismus "CPU pipeline" je odlišný mezi různými modely procesorů. Běžný ajťák nezná a nepotřebuje vědět, jak procesorová pipelina konkrétního procesoru funguje.  