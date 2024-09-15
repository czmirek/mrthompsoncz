---
draft: false
title: Celočíselné rozsahy
weight: 807
---

V IT jsou zavedené rozsahy, se kterými se většinou pracuje při práci s celými čísly. V praxi už dnes není tolik důležité se zabývat tím, jaký rozsah vybrat.

## 2<sup>8</sup>, bajt

2<sup>8</sup> je bajt (anglicky byte) a to je prostě a jednoduše číslo, které je na fyzické úrovni reprezentované osmi bity.

Je to číslo mezi 00000000 a 11111111 což je v desítkové číselné soustavě číslo mezi 0 až 255 ale velmi často je tím myšlen i rozsah mezi 1 až 256.

Bajt se znaménkem se moc nepoužívá. Pokud ano pak se jedná o rozsah -128 až +127.

## 2<sup>16</sup>

2<sup>16</sup> se v programovacích jazycích (k těm se dostanu později) často říká `short` (nebo `int16`).

Toto je také velmi známý číselný rozsah od 0 až do 65535, někdy 1 až 65536.

Pokud jde o záporné číslo, pak se jedná o rozsah -32768 až +32767 ale použití se znaménkem není časté (stejně jako u bajtu).

## 2<sup>32</sup>

2<sup>32</sup> je nejčastěji používaný celočíselný rozsah a velice univerzálně se mu říká `integer`, `int` nebo `int32`. 

Toto je dané tím, že nejpopulárnější instrukční sada `x86` má 32 bitovou šířku instrukce a proto operace s 32 bity jsou v moderních procesorech nejvymakanější a nejrychlejší.

Tento číselný rozsah se nejčastěji používá **se znaménkem** s rozsahem -2147483648 až +2147483647 (cca -2 miliardy až +2 miliardy). To je dané tím, že tento rozsah stačí pro počítání velké většiny celočíselných hodnot, se kterými počítač operuje pro běžné použití běžnými uživateli.

"Integer" se bez znaménka se zas tak moc nepoužívá – pak by to bylo číslo mezi 0 až 4294967295 (4 a čtvrt miliardy).

## 2<sup>64</sup>

2<sup>64</sup> se často označuje za `long` nebo `int64`. Toto číslo má v desítkové soustavě 20 cifer a pamatuje si ho jenom magor. Avšak stejně jako u integeru, nejčastěji použití je **se znaménkem**.

## word

**word** označuje nějaký bitový rozsah, záleží na kontextu. "word" originálně znamená bitový rozsah, s jakým pracuje procesor (v dnešní době 32/64). V moderním programování se to (aspoň co vím) už moc nepoužívá. Běžný ajťák se s tímto pojmem tak často nesetká.

## Neznámý rozsah

Může se stát, že pracujete s číslem ale nevíte, jaký rozsah v paměti je pro toto číslo rezervovaný. Toto už je v dnešní době celkem exotický problém hlavně díky tomu, že `int32`/`int64` jsou už obrovsky rozšířené standardy používané v drtivé většině všech fyzických zařízení.

Běžný ajťák v dnešní době s neznámými celočíselnými rozsahy většinou nepracuje.