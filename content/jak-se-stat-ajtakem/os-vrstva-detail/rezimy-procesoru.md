---
draft: true
title: Režimy procesoru
weight: 200300
---

Procesor má plnou kontrolu nad celým počítačem. Stačí jedna špatná instrukce a celý počítač se může kompletně zaseknout, restartovat či vypnout. Teoreticky je možné skrz instrukce pro procesor libovolnou komponentu **fyzicky zničit** nebo minimálně **trvale znemožnit další fungování**.

Z toho důvodu moderní instrukční sady začaly podporovat kategorizaci instrukcí podle jakési *citlivosti na celkový systém*. Tímto způsobem šly naproti trendu v době, kdy se počítače a procesory začaly zesložiťovat a začaly vznikat první operační systémy. 

OS mají přístup ke všem instrukcím procesoru - tomu se říká **privilegovaný režim** - zatímco programy běžící v rámci OS přístup k citlivým instrukcím nemají - tomu se říká **uživatelský režim**. Přechod z jednoho režimu do druhého je normální instrukce (kterou ale může spustit pouze ).