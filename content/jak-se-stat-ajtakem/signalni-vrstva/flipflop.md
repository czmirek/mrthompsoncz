---
draft: false
title: Flip-flop
weight: 350
---

Flip-flop je hradlové schéma, díky kterému můžete uložit bit.

![Flip flop schéma](/jak-se-stat-ajtakem/signalni-vrstva/flipflop.gif)

Všimněte si, že jakmile přijde signál, flip-flop změní stav. Pokud signál zase zmizí, stav flip-flopu zůstane stejný. Signály na vstupu fungují jako spínače pro změnu stavu.

K čemu je to dobré? Flip-flop je 1 bitová paměť. Spínačema na vstupu můžete změnit hodnotu bitu buď na 0 nebo na 1.

Narvěte vedle sebe těchto flip-flopů několik miliard a máte moderní RAM paměť.

## Flip-flop bez proudu = ztráta paměti

Všimněte si, že flip-flop drží stav na signální úrovni. V těchto obvodech musí být neustále signál, v počítačích je to zajištěné elektrickým proudem.

Pokud však počítač vypnete a elektrický proud zmizí, zmizí i signál a flip-flop zapomene, jaký signál v něm byl. Takto je implementovaná RAM paměť v počítači, která je sice velice rychlá (protože to jsou jenom držící se elektrické signály) ale závislá na elektřině. Bez elektřiny o veškerý obsah v této paměti přijdete.

## Shrnutí

- Flip-flop je hradlové schéma které umožňuje zapamatování si 1 bitu
- Po vypnutí proudu flip-flop zapomene, který bit v něm byl