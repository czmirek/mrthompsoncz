---
draft: false
title: Celá čísla
weight: 804
---

Celé číslo je z matematiky číslo, které může být buď:

- přirozené číslo (1, 2, 3 …)
- nula (0)
- záporné číslo (-1, -2, -3 ….)

V počítačích se však pracuje s celými čísly pouze dvěma způsoby:

- **celé číslo bez znaménka** = (0, 1, 2, 3…) = nerozlišujeme kladná ani záporná čísla (nebo je považujeme pouze za kladná)
- **celé číslo se znaménkem** = (…, -2, -1, 0, 1, 2….) = rozlišujeme i znaménko. Toto popíšu až v příští kapitole.

## Bitový rozsah celých čísel

V počítačích jsou celá čísla vždy spojena **s nějakým konkrétním bitovým rozsahem**. 

To znamená, že pokud v počítači pracujete s jakýmkoliv číslem tak vždycky víte, že toto číslo má vždy nějaké minimum a maximum tzn. to číslo nemůže být menší nebo větší než nějaká konkrétní hodnota.

<div class="note-blue">

**Příklad**:

Řekněme, že chcete uložit do paměti číslo 999. Kolik bitů na takové číslo potřebujete?

**Řešení**:

1) Nejdřív musíte převést číslo do dvojkové soustavy.
2) 999<sub>10</sub> = 1111100111<sub>2</sub>
3) Teď spočítejte cifry výsledku ve dvojkové soustavě
4) Pro uložení čísla 999 potřebujete minimálně 10 bitů kde minimum je 0 a maximum je 1024 (= 2<sup>10</sup>).
</div>

## Práce s kladnými čísly

Uložení celého kladného čísla (nebo nuly) je v počítači stejné jako kdybychom převáděli číslo mezi číselnými soustavami. Číslo v příkladu výše 999 se uloží jako `1111100111`.

Pokud v paměti pro tuto hodnotu vymezíme 10 bitů tak to znamená, že nejvyšší číslo, které v tomto prostoru můžeme uložit, je 2<sup>10</sup> tedy 1024. Ve dvojkové soustavě to bude 10 jedniček: `1111111111`.

## Souhrn

- Počítače pracují buď s celými čísly bez znaménka nebo se znaménkem
- Celá čísla bez znaménka jsou v paměti uložena přesně tak, jako kdybychom prováděli matematický převod mezi desítkovou a dvojkovou číselnou soustavou.
