---
draft: false
title: Plovoucí desetinná čárka
weight: 7100
description: Jak lze v počítačích uložit desetinné číslo pomocí plovoucí desetinné čárky a co je IEEE 754
---

## IEEE 754

IEEE je organizace v USA která vymýšlí různé standardy a jeden z těchto standardů je na uložení desetinného čísla pomocí techniky plovoucí desetinné čárky s názvem IEEE 754. Tento způsob vyjádření desetinných čísel s používá v každém moderním počítači.

### Jak to funguje?

Každé desetinné číslo lze reprezentovat tímto vzorečkem:

**Desetinné číslo = mantisa * 10<sup>exponent</sup>**

Například:

**1,2345 = 12345 * 10<sup>-4</sup>**

Hodnota desetinného čísla IEEE 754 se ukládá buď do 32 nebo 64 bitů a je rozdělena na další 3 hodnoty: znaménko, exponent a mantisa. Na obrázku níže je ukázka tohoto rozdělení na 64 bitech.

<div style="background-color:white;">

{{< figure align=center width=700 src="../ieee754.svg" title="" >}}

</div>

- První bit je znaménko *(ano, z toho plyne negativní a pozitivní nula, viz. níže)*
- Dalších 11 bitů je exponent
- Zbylých 52 bitů je mantisa

### Podivné hodnoty, se kterými IEEE 754 počítá

#### Kladná a záporná nula

První bit je znaménko, z toho plyne kladná a záporná nula.

Lidé z IEEE dospěli k závěru, že je jednodušší vymyslet standard, ve kterém je kladná/záporná nějak zahrnuta (a ignorována), než vymýšlet variantu dvojkového doplňku fungujícího pro desetinná čísla.

#### Kladné a záporné nekonečno

IEEE 754 obsahuje reprezentaci kladného nekonečna +∞ a záporného nekonečna -∞ a určuje, jak se s těmito hodnotami má nakládat při výpočtech s ostatními hodnotami.

#### Kladné a záporné `NaN`

`NaN` znamená "Not a Number", jinými slovy: "Toto není platné číslo". 

Tato hodnota reprezentuje nesmysl, který dokonce může být kladný nebo záporný. Tuto hodnotu lze získat například při dělení nulou.