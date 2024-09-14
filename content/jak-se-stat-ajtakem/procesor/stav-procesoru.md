---
draft: false
title: Stav procesoru
weight: 707
---

Ihned po zapnutí počítače zůstává procesor vypnutý [^o]. Procesor je z historických důvodů [^h] postavený tak, že při svém zapnutí okamžitě příjmá instrukce a jakmile je všechny spustí až do konce, tak se zase vypne.

Při zapnutí počítače však není možné, aby procesor přijímal instrukce protože není vůbec jasné, odkud se ty instrukce mají vzít.

O to se v moderních počítačích stará základní deska. Jakmile základní deska zjistí, odkud má procesor číst instrukce tak procesor zapne a rovnou mu řekne, kde se instrukce nachází.

Jakmile však procesor dojde s instrukcemi až na konec tak se procesor zase vypne [^o]. Toto se však v moderních počítačích může projevit různě: celý počítač se může vypnout nebo restartovat.

{{< figure align=center width=600 src="../stav-procesoru.png" title="Stav procesoru" >}}

U moderního počítače se totiž **neočekává, že procesor dojde až na konec instrukcí**.

[^o]: "Vypne" zde může znamenat odpojení elektrického obvodu ale i přechod do nějakého speciálního stavu, který je s vypnutím identický.

[^h]: S historickými počítači se takto reálně pracovalo. Instrukce byly předpřipravené na nějakých médiích, které se do počítače nejdřív musely fyzicky napojit. Poté se počítač spustil a hned začal provádět zadané instrukce. Po poslední instrukci se zařízení buď vyplo, nebo muselo být odpojeno.