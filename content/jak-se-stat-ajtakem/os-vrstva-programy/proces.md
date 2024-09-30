---
draft: false
title: Proces
weight: 200600
---

Po nalezení entry pointu se pro program vytvoří nový **proces**. Proces je pouze něco jako evidenční záznam který shromažďuje důležité informace pro další věci, které se v rámci procesu dějí.

{{< figure align=center src="../program-proces.png" width=300 title="Program a proces" >}}

Proces však není to, co běží. Je to pouze záznam v paměti OS. To, co reálně běží je **thread**.

## Stav procesu

Procesy mají stavy, jejich názvy a význam se však mezi jednotlivými OS liší. Jejich význam je však podobný:

- **běží** = proces normálně běží
- **pozastavený** = proces je zastavený nebo pozastavený
- **
