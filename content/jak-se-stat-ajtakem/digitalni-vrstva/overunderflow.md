---
draft: false
title: Přetečení (overflow) a podtečení (underflow)
weight: 440
---

Teď už víte, že procesor pracuje s čísly v nějakém rozsahu. Zároveň víte, jak procesory pracují s negativními čísly přes dvojkový doplněk.

## Co se stane, když výsledek matematické operace je větší, než rozsah výsledného čísla?

Co když chcete sečíst 100 + 54 a uložit jej do bajtu, který pracuje ve dvojkovém doplňku? Bajt ve dvojkovém doplňku dovoluje pouze hodnoty od -128 do +127. Číslo 154 se tam nevejde.

Máte na výběr.

- Výsledek můžete uložit do čísla s větším rozsahem, například jako integer (2<sup>32</sup>)
- Výsledek se pokusíte narvat do bajtu – dojde k přetečení

Přetečení je to, co se stane, když výsledek operace přesahuje rozsah, do kterého se číslo vejde. (Podtečení je totéž ale na druhou stranu, když je číslo menší, než je záporná hranice čísla.)

100 + 54 = 154 matematicky vypadá takto.

- 100 = 11001000
- 54 = 00110110
- 154 = 10011010

Jenže ve dvojkovém doplňku to vypadá jinak!

- 100 = 11001000
- 54 = 00110110
- <s>154</s> = 10011010 = **-102**

## Není to problém?

To záleží.

Jako ajťák musíte dobře znát nástroje, se kterými pracujete. Některé programovací jazyky považují přetečení/podtečení za chybu, kvůli které aplikace spadne a některé považují přetečení/podtečení za vlastnost výpočetní techniky, se kterou je nutné počítat.

![Xkcd](https://imgs.xkcd.com/comics/cant_sleep.png)

## Souhrn

Souhrn

- Přetečení je situace, kdy se do čísla vymezeného určitým rozsahem snažíte narvat hodnotu, která se tam nevejde.


