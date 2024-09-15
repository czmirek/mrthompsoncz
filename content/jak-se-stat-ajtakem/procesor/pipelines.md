---
draft: false
title: CPU pipeline
weight: 704
---

Moderní procesory zpracovávají instrukce v několika krocích a to je různé procesor od procesoru. Některé procesory mohou potřebovat 10 některé až 30 kroků k vykonání některých instrukcí.

Tyto postupy si lze představit jako seznam kroků, který je potřeba dokončit pro vykonání dané instrukce. V angličtině se tomu říká **CPU pipeline**.

{{< figure align=center width=300 src="../pipeline.png" title="Cyklus procesoru" >}}

⚠️ **Důležité k zapamatování**: Mechanismus "CPU pipeline" je odlišný procesor od procesoru. Běžný ajťák nezná a nepotřebuje vědět, jak procesorová pipelina konkrétního procesoru funguje.  