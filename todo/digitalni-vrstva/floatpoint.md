---
draft: true
title: Plovoucí desetinná čárka
weight: 470
---

V minulém díle jsem pojmenoval jeden způsob, „kód“, jakým lze reprezentovat desetinná čísla v počítačích – fixní desetinná čárka. Tento způsob se v počítačích ale nepoužívá, protože nelze rozumně odhadnout, jaký by měl být poměr mezi celou a desetinnou částí.

Plovoucí desetinná čárka je další způsob, další „kód“, kterým lze desetinná čísla reprezentovat. Už z názvu je jasné, že rozdělení na celou a desetinnou část není fixní ale plovoucí nebo proměnlivé.

## IEEE 754

IEEE je organizace v USA která vymýšlí různé standardy a jeden z těchto standardů je „kód“ na plovoucí desetinnou čárku s názvem IEEE 754.

Tento způsob vyjádření desetinných čísel s používá v počítačích dodnes, v každém procesoru.

Jak to funguje?

Vychází to z toho, že každé desetinné číslo lze reprezentovat tímto vzorečkem:

Desetinné číslo = mantisa * 10<sup>exponent</sup>

Já si myslím, že tuto reprezentaci jste už někde určitě viděli na nějaké kalkulačce, i když nejste ajťáci a slovo „mantisa“ vidíte poprvé. Je to jednoduchá rovnice.

1,2345 = 12345 * 10<sup>-4</sup>

Hodnota desetinného čísla IEEE 754 se ukládá buď do 32 nebo 64 bitů a je rozdělena na další 3 hodnoty: znaménko, exponent a mantisa. Na obrázku níže je ukázka tohoto rozdělení na 64 bitech.

<div style="background-color:white;">

![IEEE 754](/jak-se-stat-ajtakem/digitalni-vrstva/ieee754.svg)

</div>

- První bit je znaménko (ano, z toho plyne negativní a pozitivní nula, viz. níže)
- Dalších 11 bitů je exponent
- Zbylých 52 bitů je mantisa

### Podivné hodnoty, se kterými IEEE 754 počítá

#### Kladná a záporná nula

První bit je znaménko. Z předchozích kapitol už víte, že z toho plyne, že IEEE 754 podporuje kladnou a zápornou nulu.

Ajťáci z IEEE co to vymysleli si řekli, že bude jednodušší, aby se procesory nějak vypořádaly s kladnou a zápornou reprezentací nuly, než aby vymýšleli nějakou variantu „dvojkového doplňku“ pro desetinná čísla.

Tato prazvlášnost negativní a pozitivní nuly je zahlazena už v definici. Standard IEEE 754 narovinu říká, že záporná a kladná nula se mají chovat naprosto stejně, jako kdyby to byla jen jediná nula.

#### Kladné a záporné nekonečno

IEEE 754 obsahuje reprezentaci kladného nekonečna +∞ a záporného nekonečna -∞ a určuje, jak se s těmito hodnotami má nakládat při výpočtech s ostatními hodnotami.

#### Kladné a záporné NaN

NaN znamená „Not a Number“, jinými slovy: „Toto není platné číslo“. Prostě hodnota, která reprezentuje „nesmysl“…ale ne jeden nesmysl ale dokonce kladný nebo záporný nesmysl. Tuto hodnotu lze získat při některých matematických operacích, například dělení nulou.

Pokud provedete dělení nulou u celých čísel tak procesor provede nad vaším programem přerušení a pokračuje v toku instrukcí, který buď nadefinoval programátor nebo operační systém. Při dělení nulou v kontextu desetinných čísel se ale přerušení neprovádí a místo toho se vrátí hodnota NaN.

## Shrnutí

- Počítače pracují s desetinnými čísly pomocí plovoucí desetinné čárky přes standard který se jmenuje IEEE 754
- IEEE 754 ukládá desetinné číslo do 3 částí: znaménko, mantisa a exponent.
- IEEE 754 umí pracovat s „podivnými“ hodnotami:
  - Kladná a záporná nula
  - Kladné a záporné nekonečno
  - Kladné a záporné NaN — NaN znamená „Není číslo“ nebo „Nesmysl“ které může vzniknout po operacích jako je dělení nulou

