---
draft: false
title: OS je program běžící ve smyčce
weight: 90020
---

Operační systémy jsou programy, které po zapnutí provádí následující kroky.

### 1.: Orientace

V prvním kroku se OS snaží zorientovat, v jakém zařízení se nachází, jaké v něm jsou komponenty a podobně.

### 2.: Konfigurace

V dalším kroku (různě promíchaným s prvním krokem) provádí napříč hardwarovým systémem konfigurace a nastavení.

### 3. Vstup do OS smyčky

Zde začíná OS vrstva, ve které pracuje většina běžných uživatelů i běžných ajťáků.

### 4. Vypnutí/restartování počítače

Po vystoupení s hlavní smyčky se počítač buď vypne, restartuje, uvede do spánkového režimu, atd. v závislosti na volbě uživatele.

## Smyčka OS programu

Instrukce operačního systému se točí ve smyčce (viz. [JUMP instrukce]({{< ref "../procesor/ridici-instrukce" >}})). Operační systém je naprogramovaný tak, že v této smyčce se točí do té doby, dokud mu to uživatel (nebo jiný mechanismus) neřekne. 

Jakmile uživatel takovou instrukci zadá, operační systém z této smyčky vystoupí a spustí se instrukce které zaúkolují základní desku, aby počítač vypla (nebo restartovala, nebo dala do režimu spánku, atd.).