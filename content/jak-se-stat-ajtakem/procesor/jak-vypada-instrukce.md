---
draft: false
title: Jak vypadá instrukce
weight: 70090
---

Předpokládejme, že máme nějaký starší procesor s **fixní délkou instrukce** 16 bitů.

Do tohoto procesoru se může poslat následující instrukce.

<span style="color:orange">1011</span><span style="color:red">101001101011</span>

Tato instrukce se skládá ze dvou částí:

- <span style="color:orange">**opcode**</span> – toto je identifikátor konkrétní instrukce.
- <span style="color:red">**data**</span> – data obsahují další parametry k instrukci. Může jít například o adresu v paměti nebo konkrétní hodnotu která se má někam uložit, například pro dokončení nějaké matematické operace.