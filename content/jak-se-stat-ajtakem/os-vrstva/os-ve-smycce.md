---
draft: false
title: OS je program běžící ve smyčce
weight: 90020
---

Ještě jednu věc z kapitoly [Program]({{< relref "../procesor/program" >}}) je nutné zopakovat a zdůraznit.

Operační systémy jsou programy, které po zapnutí:

1. se nejdřív snaží zorientovat, v jakém zařízení se nachází, jaké v něm jsou komponenty a podobně
1. spustí všechny možné konfigurace a nastavení na úrovni hardwaru
1. **vstoupí do smyčky** - zde začíná OS vrstva, ve které pracuje většina běžných uživatelů i běžných ajťáků 
1. po vystoupení s hlavní smyčky se počítač buď vypne, restartuje, uvede do spánkového režimu, atd. v závislosti na volbě uživatele

Kdyby operační systémy tuto smyčku neměly tak by procesor přečetl všechny instrukce daného programu až do konce, načež by se následně počítač buď vypnul, restartoval nebo vrátil do BIOS/UEFI jak jsem popsal v kapitole [Stav procesoru]({{< relref "../procesor/stav-procesoru" >}}).