---
draft: false
title: Celočíselné rozsahy
weight: 7070
---

V IT jsou zavedené rozsahy, se kterými se většinou pracuje při práci s celými čísly ale i s jakýmkoliv jiným typem dat. V moderní praxi už většinou není důležité se rozsahy příliš zabývat.

## 2<sup>8</sup>, bajt

2<sup>8</sup> je bajt (anglicky byte) = 8 bitů.

Je to číslo mezi 00000000<sub>2</sub> a 11111111<sub>2</sub> což je v desítkové číselné soustavě číslo mezi 0<sub>10</sub> až 255<sub>10</sub> ale velmi často je tím myšlen i rozsah mezi 1<sub>10</sub> až 256<sub>10</sub>.

Bajt se znaménkem se moc nepoužívá. Pokud ano pak se jedná o rozsah -128 až +127.

## 2<sup>16</sup>

2<sup>16</sup> se v programovacích jazycích často říká `short` nebo `int16`. Také je to velmi známý číselný rozsah od 0 až do 65535, někdy 1 až 65536.

Použití se znaménkem není časté. Pokud jde o záporné číslo, pak se jedná o rozsah -32768 až +32767.

## 2<sup>32</sup>

<div class="note-blue">

⚠️ 2<sup>32</sup> je nejčastěji používaný celočíselný rozsah a velice univerzálně se mu říká `integer`, `int` nebo `int32`. 

</div>

Toto je díky tomu, že po IT revoluci v 90. letech byly velmi dlouho populární procesory s 32 bitovou šířku instrukce. Operace s 32 bity jsou v moderních procesorech nejvymakanější a nejrychlejší.

Tento číselný rozsah se nejčastěji používá **se znaménkem** s rozsahem -2147483648 až +2147483647 (cca -2 miliardy až +2 miliardy). Tento rozsah stačí pro počítání velké většiny celočíselných hodnot, se kterými počítač běžně pracuje.

Integer se bez znaménka se zas tak moc nepoužívá – pak by to bylo číslo mezi 0 až 4294967295 (4 a čtvrt miliardy).

## 2<sup>64</sup>

2<sup>64</sup> se často označuje za `long` nebo `int64`. Toto číslo má v desítkové soustavě 20 cifer. Nejčastěji použití je **se znaménkem**.

## word

`word` označuje nějaký bitový rozsah, záleží na kontextu. `word` originálně znamená bitový rozsah, s jakým pracuje procesor (v dnešní době 32/64). V moderním programování se tento pojem už moc nepoužívá.

## Neznámý rozsah

Může se stát, že pracujete s číslem ale nevíte, jaký rozsah v paměti je pro toto číslo rezervovaný. V dnešní době se jedná o exotický problém hlavně díky tomu, že `int32`/`int64` jsou už obrovsky rozšířené standardy používané v drtivé většině všech fyzických zařízení.

Běžný ajťák v dnešní době s neznámými celočíselnými rozsahy většinou nepracuje.