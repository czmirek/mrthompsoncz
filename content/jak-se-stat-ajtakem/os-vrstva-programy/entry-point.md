---
draft: false
title: Entry point
weight: 200500
---

Při spuštění jakéhokoliv programu nejdřív OS najde kompatibilní **entry point** což je jinými slovy místo, kde pro daný program začínají instrukce, které mohou začít proudit do procesoru.

Entry point se odvíjí od [**binárního formátu programu**]({{< relref "program-format" >}}) (viz předchozí kapitola). Z tohoto důvodu není možné aplikaci na Windows spustit např. na macOS a naopak.

{{< figure align=center src="../entry-point.png" width=200 title="Entry point v programu" >}}