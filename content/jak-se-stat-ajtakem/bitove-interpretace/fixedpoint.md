---
draft: false
title: Fixní desetinná čárka
weight: 7090
---

Jeden způsob uložení desetinného čísla je **fixní desetinná čárka**.

## Příklad

Řekněme, že máte 32 bitů.
`00000000000000000000000000000000`

Jak do toho uložíte třeba číslo pí, které si zaokrouhlíme na `3,14`?

Desetinné číslo se skládá z celé a desetinné části, tedy `3` a `14` a to převedeme do dvojkové soustavy.

- 3<sub>10</sub> = 11<sub>2</sub>
- 14<sub>10</sub> = 1110<sub>2</sub>

Dále 32 bitů rozdělíte na dvě skupiny: na celou a desetinnou část, třeba půl na půl: 16 bitů pro celou část, 16 bitů pro desetinnou část

<span style="color:red">0000000000000011</span>: celá část  
<span style="color:orange">0000000000001110</span>: desetinná část  
**3,14** = <span style="color:red">0000000000000011</span><span style="color:orange">0000000000001110</span>

Tento způsob není moc užitečný z několika důvodů

- Pokud procesor postavíte nad fixní desetinnou čárkou, nemáte možnost to později změnit.
- Musíte při výrobě procesoru odhadnout, jak velká by měla být celá část a jak velká desetinná část. Jedno je na úkor druhého. Různá odvětví vyžadují různě přesná/velká čísla, proto musíte vymyslet jiné řešení. Viz. další kapitola.