---
draft: false
title: Synchronní I/O instrukce
weight: 70710
---

U běžných počítačů můžete předpokládat, že procesor dokáže komunikovat s každou komponentou - tzn. s každým vstupem a výstupem - napřímo.

Tzn. procesor je schopný na základě dané instrukce přečíst nebo zapsat data do jakékoliv jiné komponenty v systému.

{{< figure align=center width=500 src="../syncio2.png" title="Sybchronní komunikace" >}}

Nevýhoda tohoto způsobu spočívá v tom, že instrukce plýtvá obrovské množství cyklů protože jakékoliv I/O zařízení je řádově pomalejší, než samotný procesor.

Zatímco procesor pracuje v rychlostech miliardy cyklů za vteřinu tak ostatní komponenty jsou vždy pomalejší. Procesor tak čekáním může vyplýtvat klidně celé miliardy cyklů. U běžného použití to znamená, že se počítač může reálně "kousnout" protože čeká na nějaké zařízení.

Z tohoto důvodu se synchronní I/O instrukce nepoužívají.
