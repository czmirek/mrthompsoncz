---
draft: false
title: Proces
weight: 200600
---

Po nalezení entry pointu se pro program vytvoří nový **proces**. Proces je pouze něco jako evidenční záznam který shromažďuje důležité informace pro další věci, které se v rámci procesu dějí.

{{< figure align=center src="../program-proces.png" width=300 title="Program a proces" >}}

Technicky správné označení je "proces" ale běžným označením je i "běžící program". **Proces ale reálně není to, co běží.** Proces je pouze záznam v paměti OS. To, co reálně běží je **vlákno** neboli **thread**.