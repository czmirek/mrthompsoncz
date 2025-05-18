---
draft: false
title: Flip-flop
weight: 502
description: Jak lze skrz hradla vytvořit flip-flop který reprezentuje jednobitovou paměť
---

Flip-flop je hradlové schéma, díky kterému můžete držet stav signálu.

{{< figure align=center width=500 src="../img/flipflop.gif" title="Flip-flop" >}}

Všimněte si, že jakmile přijde signál, flip-flop změní stav. Pokud signál zase zmizí, stav flip-flopu zůstane stejný. Signály na vstupu fungují jako spínače pro změnu stavu.

K čemu je to dobré? **Flip-flop je 1 bitová paměť.** Spínači na vstupu můžete změnit hodnotu signálu. 

## Flip-flop bez proudu = ztráta paměti

Flip-flop je jen jiný pohled na elektrické obvody, které musí být neustále pod proudem, aby flip-flop fungoval.

<div class="note-blue">

⚠️ Pokud počítač vypnete a elektrický proud zmizí, **zmizí i signál a flip-flop zapomene, jaký signál v něm byl**. 

⚠️ Pomocí flip-flopů je implementovaná RAM paměť v počítači, která je sice velice rychlá ale závislá na elektřině.

⚠️ Bez elektřiny veškerý obsah z RAM paměti zmizí.

</div>