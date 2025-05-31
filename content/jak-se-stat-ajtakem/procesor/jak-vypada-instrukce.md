---
draft: false
title: Jak vypadá instrukce
weight: 70120
description: Podrobný pohled na instrukce
---

Předpokládejme, že máme nějaký starší 16 bitový procesor, tedy procesor, do kterého mohou téct pouze 16 bitové instrukce.

Jedna instrukce může vypadat například takto.

<span style="color:orange">1011</span><span style="color:red">101001101011</span>

<div class="note-blue">

Instrukce se skládá ze dvou částí:

- <span style="color:orange">**opcode**</span> – toto je identifikátor konkrétní instrukce.
- <span style="color:red">**data**</span> – data obsahují další parametry k instrukci. Může jít například o adresu v paměti nebo konkrétní hodnotu která se má někam uložit, například pro dokončení nějaké matematické operace.

</div>