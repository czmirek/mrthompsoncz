---
draft: false
title: RAM paměť
weight: 770
---

RAM paměť je extrémně rychlá [^a] [^b], dokáže fungovat na vysokých frekvencích avšak za cenu toho, že po odpojení z elektřiny - tedy po vypnutí počítače - jakékoliv informace z RAM paměti zmizí (viz. [Flip-flop]({{< relref "../hradlova-vrstva/flipflop" >}} "Flip-Flop")).

Procesor **za běžného provozu** čte svoje instrukce hlavně z RAM paměti. To samozřejmě vede k otázce: **odkud procesor vezme instrukce, když je RAM paměť po zapnutí počítače prázdná?**

## Načtení instrukcí do RAM

Odpověď souvisí s kapitolou [Stav procesoru]({{< ref "stav-procesoru" >}} "Stav procesoru"). Po zapnutí počítače se **základní deska** snaží zjistit, kde se instrukce pro procesor nachází. Jakmile je najde, pravděpodobně na nějakém persistentním uložišti jako je SSD nebo HDD disk tak tyto instrukce přesune do RAM paměti. 

Poté základní deska předává otěže procesoru. Jak už víte z předchozích dílů, procesor pak naivně postupuje podle zadaných instrukcí, které obdrží v RAM paměti, jednu po druhé.  

## Dokáže procesor číst instrukce z jiného zařízení?

V tuto chvíli si ještě nebavíme o operačních systémech. Pohybujeme se na bitové úrovni tzn. žádný operační systém nemáme k dispozici, zabýváme se pouze tím, jak procesor funguje a co dokáže.

Na bitové úrovni můžeme předpokládat, že procesor v počítači dokáže **úplně všechno**. [^u]

Stejně tak dokáže i načíst instrukce z jiného místa, než jen z RAM paměti, běžně se to ale nedělá protože jakýkoliv jiný zdroj instrukcí je **řádově pomalejší** než procesor.

Procesor je schopný zpracovat miliardy instrukcí za vteřinu. Pokud by se procesor snažil číst instrukce z jiného uložiště, než z RAM paměti, dramaticky by se zpomalil. Běžné načtení instrukce z RAM trvá jednotky až desítky cyklů zatímco z jiného uložiště by toto mohlo trvat tisíce až miliony cyklů.


[^a]: *Moderní RAM paměť funguje na vysokých frekvencích avšak ne na stejných frekvencích jako procesor. Procesor má navíc své vlastní "paměťi" (zvané *cache*) které v několika úrovních s RAM pamětí synchronizuje.*

[^b]: *Komunikace mezi procesorem a RAM pamětí je tak důležitá že z toho vznikla řada samostatných standardů které musí být společně podporovány procesorem, chipsetem základní desky a samotnými moduly RAM paměti. Jinak hrozí, že RAM paměť - i když je schopná běžet rychleji - poběží podle pomalejšího standardu protože procesor nebo chipset základní desky tento standard nepodporuje.*

[^u]: *Většina procesorů. Pravděpodobně. Detaily toho, co procesory reálně umí a neumí nejsou pro běžného ajťáka zas tak podstatné.*