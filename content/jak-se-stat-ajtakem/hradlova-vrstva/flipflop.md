---
draft: false
title: Flip-flop
weight: 502
---

Flip-flop je hradlové schéma, díky kterému můžete uložit bit (stav signálu 0 nebo 1).

{{< figure align=center width=500 src="../img/flipflop.gif" title="Flip-flop" >}}

Všimněte si, že jakmile přijde signál, flip-flop změní stav. Pokud signál zase zmizí, stav flip-flopu zůstane stejný. Signály na vstupu fungují jako spínače pro změnu stavu.

K čemu je to dobré? **Flip-flop je 1 bitová paměť.** Spínačema na vstupu můžete změnit hodnotu bitu buď na 0 nebo na 1.

Narvěte vedle sebe těchto flip-flopů několik miliard a máte moderní RAM paměť.

## Flip-flop bez proudu = ztráta paměti

Flip-flop je jen jiný pohled na elektrické obvody, které musí být neustále pod proudem, aby flip-flop fungoval.

Pokud však počítač vypnete a elektrický proud zmizí, **zmizí i signál a flip-flop zapomene, jaký signál v něm byl**. Takto je implementovaná RAM paměť v počítači, která je sice velice rychlá (protože to jsou jenom držící se elektrické signály) ale závislá na elektřině. 

Bez elektřiny veškerý obsah z RAM paměti zmizí.