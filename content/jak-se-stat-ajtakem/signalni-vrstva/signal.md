---
draft: false
title: Signál
weight: 401
---

Běžný ajťák se příliš nezabývá fyzickou ani elektronickou vrstvou. Před postupem do digitální vrstvy je však nutné pochopit ještě signální vrstvu.

**Signál je způsob předání či uchování informace v elektronických obvodech**. Nejjednodušší možnost předávání informací v elektronických obvodech spočívá v rozdílu dvou úrovní napětí.

{{< figure align=center width=500 src="../signal1.png" title="Signál" >}}

Na základě tohoto rozdílu lze pak definovat nějaký "kód" --- tento kód je podstatou digitální vrstvy.


## Morseovka[^m]

**Morseovka se v počítačích <u>nepoužívá</u>**. Skvěle se na ní vysvětluje signální vrstva ještě před tím, než se vrhneme do digitální vrstvy.

Morseovka je vlastně nějaký kód, kterým můžeme interpretovat elektronickou vrstvu. V minulých stoletích se morseovkou na elektrické vrstvě reálně komunikovalo.

Morseovka má krátký signál a dlouhý signál. Na obrázku výše je pak písmeno "Y" které má v morseovce kód `-.--`. Na drátě je však potřeba mít ještě třetí stav: když se nic nevysílá. Ten může být reprezentovaný 0 volty tzn. v drátu není žádné napětí.

{{< figure align=center width=500 src="../y.png" title="Signál" >}}

[^m]: Pamatujte si, že morseovku používám jen jako učební nástroj. Morseovka se v počítačích nepoužívá.