---
draft: false
title: Souběžnost programů
weight: 200100
---

V minulé kapitole jsem řekl, že operační systém umožňuje paralelní běh více progamů najednou.

Toto je rozdíl oproti [bare-metal programování]({{< relref "../os-vrstva-bit/bare-metal-programming" >}}). Procesor samotný - respektive každé procesorové jádro - dokáže rozeběhnout pouze **jeden jediný program**. Operační systém ale umožňuje **souběžný běh více programů najednou** a to i na **jednojádrovém procesoru**. [^1]

{{< figure align=center width=700 src="../soubeznost.png" title="Souběžnosti programů" >}}

[^1]: *Pokud vám to naprosto nedává smysl a ptáte se, jak je to vůbec logicky možné, tak čtěte dál, píšu o tom v pozdější kapitole.*