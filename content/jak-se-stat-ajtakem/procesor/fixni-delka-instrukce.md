---
draft: false
title: Fixní délka instrukce
weight: 709
---

Předpokládejme, že máme nějaký starší procesor s **fixní délkou instrukce** 16 bitů.

Do tohoto procesoru se může poslat následující instrukce.

<span style="color:orange">1011</span><span style="color:red">101001101011</span>

Tato instrukce se skládá ze dvou částí:

- <span style="color:orange">**typ instrukce**</span> – toto říká, co procesor má udělat.
- <span style="color:red">**data**</span> – většina instrukcí vyžaduje ještě nějaké informace navíc. Může jít například o adresu v paměti nebo konkrétní hodnotu která se má někam uložit, například pro dokončení nějaké matematické operace.