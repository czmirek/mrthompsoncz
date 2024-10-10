---
draft: false
title: Mode switch
weight: 201300
---

V minulém díle jsem pojmenoval dva režimy CPU - **privilegovaný režim** a **uživatelský režim**.

<div class="note-blue">

⚠️ **Důležité k zapamatování:** 
- OS samotné běží v privilegovaném režimu. 
- **Všechny** programy v OS  běží v **uživatelském režimu**. [^s]
</div>

Jakýkoliv pokus o přímou komunikaci s jakoukoliv komponentou CPU zablokuje a oznámí to OS. Ve výsledku to OS interpretuje jako chybu procesu.

Nezapomeňte, že OS sdílí kapacitu procesoru s ostatními programy. Aby OS mohl dělat svojí práci, nastavuje si v procesoru **privilegovaný režim** ale všem ostatním programům v rámci multithreadingu nastavuje **uživatelský režim**.

**Mode switch** je moment, kdy OS přepne procesor z privilegovaného režimu na uživatelský režim a naopak. Stejně jako u context switche, četnost této operace za vteřinu je v desítká, stovkách i tisících za vteřinu, záleží ale i na daném OS.

[^s]: *Situace se trochu komplikuje jakmile se začneme bavit o ovladačích neboli "driverech" ale to teď není důležité.*