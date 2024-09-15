---
draft: false
title: Instrukce - detailní pohled
weight: 709
---

Předpokládejme, že máme nějaký starší procesor s pevně danou 16 bitovou šířkou.

Řekněme, že se v našem 16 bitovém procesoru spouští následující instrukce.

<span style="color:orange">1011</span><span style="color:red">101001101011</span>

Tato instrukce se skládá ze dvou částí [^r]:

- <span style="color:orange">**typ instrukce**</span> – toto říká, co procesor má udělat.
- <span style="color:red">**data**</span> – většina instrukcí vyžaduje ještě nějaké informace navíc. Může jít například o adresu v paměti nebo konkrétní hodnotu která se má někam uložit, například pro dokončení nějaké matematické operace.

[^r]: Realita je v moderních instrukčních sadách o něco složitější to však není pro běžného ajťáka podstatné.