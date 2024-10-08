---
draft: false
title: Signál
weight: 401
---

Běžný ajťák se příliš nezabývá fyzickou ani elektronickou vrstvou. 

Před postupem do digitální vrstvy je však nutné pochopit ještě signální vrstvu.

## Co je signál

**Signál je způsob předání či uchování informace v elektronických obvodech**.

Nejjednodušší možnost předávání informací v elektronických obvodech spočívá ve dvou úrovních napětí.

{{< figure align=center width=500 src="../signal1.png" title="Signál" >}}

## Morseovka[^m]

Na základě toho lze definovat nějaký "kód" --- tento kód je podstatou digitální vrstvy, o které budu mluvit v další kapitole. Pod tímto "kódem" si můžete představit třeba morseovku. **Morseovka se v počítačích <u>nepoužívá</u>**, skvěle se však na ní vysvětluje signální vrstva.

Morseovka má krátký signál a dlouhý signál. Na obrázku níže je pak písmeno "Y" které má v morseovce kód `-.--`. Na drátě je však potřeba mít ještě třetí stav: když se nic nevysílá. Ten může být reprezentovaný 0 volty tzn. v drátu není žádné napětí.

{{< figure align=center width=500 src="../y.png" title="Signál" >}}

[^m]: Pamatujte si, že morseovku používám jen jako učební nástroj. Morseovka se v počítačích nepoužívá.