---
draft: false
title: Fixní desetinná čárka
weight: 1109
---

V minulém díle jsem mluvil o tom, jak počítače nedokážou reprezentovat většinu desetinných čísel přesně. Nemluvil jsem ale o tom, jak se s desetinnými čísly vlastně konkrétně v počítačích pracuje.

Jeden způsob je **fixní desetinná čárka**.

## Příklad

Řekněme, že máte 32 bitů.
`00000000000000000000000000000000`

Jak do toho uložíte třeba číslo pí, které si zaokrouhlíme na `3,14`?

- Desetinné číslo se skládá z celé a desetinné části.
- Jsou to vlastně dvě skupiny cifer: `3` a `14`.

Takže můžete prostě jednoduše říct, že tato čísla převedete do dvojkové soustavy jako celá čísla:

- 3<sub>10</sub> = 11<sub>2</sub>
- 14<sub>10</sub> = 1110<sub>2</sub>

Takže máte teď bity 11 a další bity 1110 které potřebujete nějak uložit do 32 bitů. Jak to uděláte?

Jeden možný způsob je fixní desetinná čárka.

32 bitů rozdělíte na dvě skupiny: na celou a desetinnou část, třeba půl na půl: 16 bitů pro celou část, 16 bitů pro desetinnou část

<span style="color:red">0000000000000011</span>: celá část  
<span style="color:orange">0000000000001110</span>: desetinná část  
**3,14** = <span style="color:red">0000000000000011</span><span style="color:orange">0000000000001110</span>

Tento způsob není moc užitečný z několika důvodů

- Pokud procesor postavíte nad fixní desetinnou čárkou, nemáte možnost to změnit.
- Musíte při výrobě procesoru odhadnout, jak velká by měla být celá část a jak velká desetinná část. Jedno je na úkor druhého. Jenže různá odvětví vyžadují různě přesná/velká čísla, jako výrobce procesorů si nemůžete dovolit vyrábět pro každé odvětví procesory s různě stanovenými fixními čárkami, proto musíte vymyslet jiné řešení. Viz. další kapitola.