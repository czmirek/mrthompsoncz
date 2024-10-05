---
draft: false
title: Režimy CPU
weight: 201200
---

Před další kapitolou o procesech je nutné se na chvíli vrátit k procesorům, konkrétně k **procesorovým režimům** (anglicky *CPU mode*)

Moderní procesory podporují 2 základní režimy [^a] zvané:
- **privilegovaný režim**
- **uživatelský režim**

## Privilegovaný režim
Při zapnutí počítače běží procesor v privilegovaném režimu. V tomto režimu je možné v procesoru spustit jakoukoliv instrukci bez omezení, zejména instrukce pro interakci s ostatními komponentami. OS běží v tomto režimu.

{{< figure align=center width=500 src="../privilegovany-rezim.png" title="Privilegovaný režim" >}}

## Uživatelský režim
Speciální instrukcí je možné přepnout procesor do uživatelského režimu. V tomto režimu **nemůže procesor komunikovat se žádnou komponentou napřímo** minimálně do té doby, dokud další speciální instrukcí nedojde k přepnutí zpět do privilegovaného režimu.

{{< figure align=center width=500 src="../uzivatelsky-rezim.png" title="Uživatelský režim" >}}

⚠️ **Důležité k zapamatování:** V uživatelském režimu běží **všechny** procesy spuštěné v rámci OS [^s]. Pokud se jakýkoliv proces běžící v OS pokusí o přímou komunikaci s jakoukoliv komponentou tak to CPU zablokuje a ještě to napráská OS které to vyhodnotí jako chybu procesu. 

[^a]: *V rámci tohoto návodu se budeme mnohem později ještě bavit o třetím "virtualizačním" režimu*
[^s]: *Situace se trochu komplikuje jakmile se začneme bavit o ovladačích neboli "driverech" ale to teď není důležité.*