---
draft: false
title: Role RAM paměti
weight: 712
---


<div class="note-blue">

**⚠️ Důležité k zapamatování:** Procesor spouští instrukce, čte a zapisuje data **pouze z/do RAM paměti**.

Procesor nikdy nekomunikuje s žádnými ostatními komponentami napřímo a vždy pouze instruuje chipset základní desky, aby za něj do RAM paměti připravovala vše, o co si zrovna řekne.  

</div>

<br />

RAM paměť je extrémně rychlá [^a] [^b], dokáže fungovat na vysokých frekvencích avšak za cenu toho, že po odpojení z elektřiny - tedy po vypnutí počítače - jakékoliv informace z RAM paměti zmizí (viz. [Flip-flop]({{< relref "../hradlova-vrstva/flipflop" >}} "Flip-Flop")).

Procesor neumí číst instrukce ze žádného jiného zařízení jelikož všechna ostatní zařízení jsou proti procesoru extrémně pomalá.

To samozřejmě vede k otázce: **odkud procesor vezme instrukce, když je RAM paměť po zapnutí počítače prázdná?**

## Načtení instrukcí do RAM

Odpověď souvisí s kapitolou [Stav procesoru]({{< ref "stav-procesoru" >}} "Stav procesoru"). Po zapnutí počítače se základní deska snaží zjistit, kde se instrukce pro procesor nachází. Jakmile je najde, pravděpodobně na nějakém persistentním uložišti jako je SSD nebo HDD disk tak sdělí procesoru, kde se tyto instrukce nachází, na jakém zařízení a na jaké adrese tohoto zařízení.

V tuto chvíli základní deska předává otěže procesoru, který pak instruuje základní desku pro načtení těchto instrukcí z peristentního uložiště do RAM paměti. 

Jakmile je tento proces hotový tak procesor - jak už víte z předchozích dílů - začne naivně tyto instrukce číst a spouštět, jednu po druhé.

[^a]: *Moderní RAM paměť funguje na vysokých frekvencích avšak ne na stejných frekvencích jako procesor. Procesor má navíc své vlastní "paměťi" (zvané *cache*) které v několika úrovních s RAM pamětí synchronizuje.*

[^b]: *Komunikace mezi procesorem a RAM pamětí je tak důležitá že z toho vznikla řada samostatných standardů které musí být společně podporovány procesorem, chipsetem základní desky a samotnými moduly RAM paměti. Jinak hrozí, že RAM paměť - i když je schopná běžet rychleji - poběží podle pomalejšího standardu protože procesor nebo chipset základní desky tento standard nepodporuje.*