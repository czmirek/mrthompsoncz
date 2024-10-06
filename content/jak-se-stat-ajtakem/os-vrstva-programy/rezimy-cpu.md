---
draft: false
title: Režimy CPU
weight: 201200
---

Před další kapitolou o procesech je nutné se na chvíli vrátit k procesorům, konkrétně k **procesorovým režimům** (anglicky *CPU mode*). 

CPU režim si lze představit jako jakýsi stav celého procesoru. Tímto režimem se určuje, které instrukce lze spouštět a které ne.

Moderní procesory podporují 2 základní režimy [^a] zvané:
- **privilegovaný režim**
- **uživatelský režim**

## Privilegovaný režim
Při zapnutí počítače běží procesor v privilegovaném režimu. V tomto režimu je možné v procesoru spustit jakoukoliv instrukci bez omezení, zejména instrukce pro interakci s ostatními komponentami. OS běží v tomto režimu.

{{< figure align=center width=500 src="../privilegovany-rezim.png" title="Privilegovaný režim" >}}

## Uživatelský režim
Speciální instrukcí je možné přepnout procesor do uživatelského režimu. V tomto režimu **nemůže procesor komunikovat se žádnou komponentou napřímo** minimálně do té doby, dokud další speciální instrukcí nedojde k přepnutí zpět do privilegovaného režimu.

{{< figure align=center width=500 src="../uzivatelsky-rezim.png" title="Uživatelský režim" >}}

[^a]: *V rámci tohoto návodu se budeme mnohem později ještě bavit o třetím "virtualizačním" režimu*