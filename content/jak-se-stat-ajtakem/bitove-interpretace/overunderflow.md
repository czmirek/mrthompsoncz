---
draft: false
title: Přetečení a podtečení
weight: 7060
description: Co je přetečení a podtečení a proč k němu dochází při matematických operacích v počítačích
---

## Co se stane, když výsledek matematické operace je větší, než rozsah výsledného čísla?

Co když chcete sečíst 100 + 54 a uložit jej do bajtu, který pracuje ve dvojkovém doplňku? Bajt ve dvojkovém doplňku dovoluje pouze hodnoty od -128 do +127. Číslo 154 se tam nevejde.

Máte na výběr.

- Výsledek můžete uložit do čísla s větším rozsahem, například 2<sup>32</sup>
- Rozsah nezměníte – dojde k přetečení

Přetečení znamená, že výsledek operace přesahuje rozsah, do kterého se číslo vejde. Podtečení je totéž ale na druhou stranu, když je číslo menší, než je záporná hranice čísla.

100 + 54 = 154 matematicky vypadá takto.

- 100<sub>10</sub> = 11001000<sub>2</sub>
- 54<sub>10</sub> = 110110<sub>2</sub>
- 154<sub>10</sub> = 10011010<sub>2</sub>

Jenže ve dvojkovém doplňku to vypadá jinak!

- 100<sub>10</sub> = 11001000<sub>2</sub>
- 54<sub>10</sub> = 00110110<sub>2</sub>
- <s>154<sub>10</sub></s> = 10011010<sub>2</sub> = **-102<sub>10</sub>**

