Vzpomeňte si, jak funguje procesor. Toto zařízení neumí „nic nedělat“ a neustále přijímá příkazy.

První operační systémy byly velmi jednoduché programy:

![OS cyklus](/jak-se-stat-ajtakem/os-vrstva/os-cyklus.png)

Všimněte si, že tato jednoduchá aplikace je v nekonečné smyčce. Pokud by operační systém skončil, procesor by přestával dostávat instrukce a v důsledku toho by se celý počítač vypnul, nebo se restartoval.*

Moderní OS, přestože jsou řádově komplexnější a složitější, také běží v nekonečné smyčce, v případě Linuxu to jsou minimálně 2 vlákna v nekonečných smyčkách:

- Uživatelské vlákno, které čeká na vstupy od uživatele
- „Čekací vlákno“ (v Linuxu pojmenované jako „idle loop“) které předává procesoru instrukci pro „nic nedělání“ v případě, že procesor nemá dost věcí na práci. (a v případě, že procesor instrukci pro „nic nedělání“ podporuje. Pokud ne, Linuxy předají procesoru nesmyslné ale neškodné instrukce.)

<div class="note1">

*V dnešní době by se počítač nevypnul ani automaticky nerestartoval. Počítače v dnešní době mají v sobě UEFI nebo minimálně BIOS, což jsou vlastně velmi omezené OS pro základní správu zařízení integrované přímo v čipech na základních deskách počítačů.

</div>

## Shrnutí

- Operační systémy jsou programy, které běží v nekonečné smyčce, ve které čekají na uživatelský vstup.