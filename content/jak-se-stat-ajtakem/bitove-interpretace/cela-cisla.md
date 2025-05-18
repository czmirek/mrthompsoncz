---
draft: false
title: Celá čísla
weight: 7040
description: Jak v počítačích fungují celá čísla
---

Celé číslo je z matematiky číslo, které může být buď:

- přirozené číslo (1, 2, 3 …)
- nula (0)
- záporné číslo (-1, -2, -3 ….)

V počítačích se však pracuje s celými čísly pouze dvěma způsoby:

- **celé číslo bez znaménka** = (0, 1, 2, 3…) = nerozlišujeme kladná ani záporná čísla, nebo je považujeme pouze za kladná
- **celé číslo se znaménkem** = (…, -2, -1, 0, 1, 2….) = rozlišujeme i znaménko

## Bitový rozsah celých čísel

V počítačích jsou celá čísla vždy spojena **s nějakým konkrétním bitovým rozsahem**. Z toho plyne, že celá čísla mají vždy nějaké minimum a maximum.

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

Celá kladná čísla se v počítačích ukládají stejně, jako kdybychom jen převáděli mezi číselnými soustavami. 

Číslo 999<sub>10</sub> se uloží jako 1111100111<sub>2</sub>.

Pokud v paměti pro tuto hodnotu vymezíme 10 bitů tak to znamená, že nejvyšší číslo, které v tomto prostoru můžeme uložit, je 2<sup>10</sup> tedy 1024<sub>10</sub> tedy 1111111111<sub>2</sub>.

## Souhrn

- Počítače pracují buď s celými čísly bez znaménka nebo se znaménkem
- Celá čísla bez znaménka jsou v paměti uložena přesně tak, jako kdybychom prováděli matematický převod mezi desítkovou a dvojkovou číselnou soustavou.
