---
draft: true
title: Mode switch
weight: 201300
---

V minulém díle jsem pojmenoval dva režimy CPU - **privilegovaný režim** a **uživatelský režim**.

<div class="note-blue">

⚠️ **Důležité k zapamatování:** V uživatelském režimu běží **všechny** procesy spuštěné v rámci OS [^s] . 
</div>

Jakýkoliv pokus o přímou komunikaci s jakoukoliv komponentou CPU zablokuje a oznámí to OS. Ve výsledku to OS interpretuje jako chybu procesu a ukončí jej.

[^s]: *Situace se trochu komplikuje jakmile se začneme bavit o ovladačích neboli "driverech" ale to teď není důležité.*