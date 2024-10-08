---
draft: false
title: Přetečení a podtečení
weight: 7060
---

## Co se stane, když výsledek matematické operace je větší, než rozsah výsledného čísla?

Co když chcete sečíst 100 + 54 a uložit jej do bajtu, který pracuje ve dvojkovém doplňku? Bajt ve dvojkovém doplňku dovoluje pouze hodnoty od -128 do +127. Číslo 154 se tam nevejde.

Máte na výběr.

- Výsledek můžete uložit do čísla s větším rozsahem, například jako integer (2<sup>32</sup>)
- Výsledek se pokusíte narvat do bajtu – dojde k přetečení

Přetečení je to, co se stane, když výsledek operace přesahuje rozsah, do kterého se číslo vejde. (Podtečení je totéž ale na druhou stranu, když je číslo menší, než je záporná hranice čísla.)

100 + 54 = 154 matematicky vypadá takto.

- 100 = 11001000
- 54 = 110110
- 154 = 10011010

Jenže ve dvojkovém doplňku to vypadá jinak!

- 100 = 11001000
- 54 = 00110110
- <s>154</s> = 10011010 = **-102**

## Není to problém?

Není.

Jako ajťák však musíte dobře znát nástroje, se kterými pracujete. O přetečení a podtečení se budeme bavit ještě znovu až v kapitolách o tvorbě softwaru.

![Xkcd](https://imgs.xkcd.com/comics/cant_sleep.png)

