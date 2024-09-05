---
draft: false
title: Software a OS
weight: 905
---

Aby software běžící v OS mohl nějakým způsobem interagovat se zařízením – například interagovat s pamětí, s disky, reagovat na stisk klávesnice, musí využít funkce nebo události OS.

Tyto funkce a události souhrně nazývám „nízko-úrovňové“ protože při běžném programování jsou OS funkce ta nejnižší dostupná úroveň. Každý operační systém je však nazývá jinak.

- Ve Windows je jeden kompaktní balík funkcí kterému se říká Win32 API.
- V Linuxu to není jeden kompaktní balík ale hromada funkcí různě rozházených v Linuxové dokumentaci, souhrnně se těmto funkcím říká syscalls (System call). To ještě zesložiťuje fakt, že neexistuje jeden Linux ale spousta různých Linuxů.

Nízko-úrovňové události jsou operačním systémem zpracovaná přerušení procesoru. Software v OS má možnost se na tyto události „navěsit“ a díky tomu zprostředkovaně reagovat na události jako je například pohyb myši nebo stisk klávesnice.

## Prostředí OS z pohledu software

OS před softwarem schovává konkrétní složitosti daného zařízení a místo toho vytváří úplně nové koncepty. Podívejte se na tabulku níže. V této kapitole jsem pojmenoval nízko-úrovňové funkce a události OS, v následujících kapitolách vysvětlím další pojmy.

<div class="note1">

<!-- 
TODO
    Zařízení	Co vidí os	co vidí software běžící v os
Fyzická RAM paměť	Fyzická RAM paměť
Kernel space
User space	Virtuální paměť
HDD/SSD disky	HDD/SSD disky
NTFS, FAT32, ext3, ext4…	Souborový systém
USB zařízení	USB zařízení
Ovladače	Nízko-úrovňové
funkce a události OS
Fyzická jádra procesoru	Fyzická jádra procesoru
Scheduler
Procesy
Vlákna
Context switch	Procesy a vlákna
-->
</div>

## Shrnutí

- Software interaguje s počítačem skrz nízkoúrovňové funkce OS
- Počítač interaguje se software skrz nízkoúrovňové události OS. Toto jsou jen delegovaná přerušení procesoru.