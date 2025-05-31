---
draft: false
title: Přesunové instrukce
weight: 70300
description: Přesunové instrukce jsou jakékoliv instrukce pro posílání bitů z jednoho místa do jiného místa
---

**Přesunové instrukce** jsou jakékoliv instrukce pro posílání bitů z jednoho místa do jiného místa.

Zjednodušeně jde o tyto přesuny:

- Z RAM paměti do jiného místa v RAM paměti
- Z RAM paměti do I/O komponenty
- Z I/O komponenty do RAM paměti
- Z I/O komponenty do jiné I/O komponenty

<div class="note-blue">

⚠️ Při interakcích se vstupními/výstupními (I/O) komponentami procesor instruuje čipset základní desky, který přesuny dat provádí místo něj. Procesor je v počítači téměř vždy nejrychlejší komponenta a nemůže si dovolit čekat na ostatní mnohem pomalejší zařízení.

O tom píšu ještě v pozdější kapitole.

</div>