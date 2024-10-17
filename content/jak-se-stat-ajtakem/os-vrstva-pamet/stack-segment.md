---
draft: false
title: Stack segment
weight: 211000
---

**Stack segment** už je trochu složitější struktura. 

<div class="note-blue">

⚠️ Porozuměmí *stacku* bude znovu důležité v kapitolách o tvorbě softwaru. Pokud čtete tento návod postupně od začátku tak podrobné porozumění *stacku* není v tuto chvíli důležité.

</div>

{{< figure align=center width=600 src="../stack-segment.png" title="Stack segment struktura" >}}

Nenechte se tím obrázkem zmást - všechno to jsou pořád jenom bity, které ve virtuální paměti utváří nějakou strukturu, se kterou procesy nějak pracují.

## Stack segment

Stack segment **není fixní** a **jeho obsahy mohou libovolně růst**.

### Call stack

Jak již víte z předchozích kapitol, každý proces obsahuje **hlavní vlákno**. Během svého provozu však může proces vytvořit libovolné množství jiných vláken, které mají na starost nějaké jiné úlohy u kterých dává smysl, aby běžely paralelně. Každé nově vytvořené vlákno procesu má **svůj vlastní call stack**, někdy se označuje také jako **thread stack**. 

Velikost call stacku **není fixní a jeho obsah může libovolně růst**.

### Stack frame

Call stack obsahuje **stack frames** které proces může libovolně přidávat a odebírát. 

Stack je "LIFO" [^l] struktura. To znamená, že stack frames jsou seřazené, jako kdybychom skládali cihly na sebe. První stack frame leží na zemi. Druhý stack frame leží na tom prvním. Třetí na tom druhém. A tak dále.

{{< figure align=center width=200 src="../cihly.png" title="Cihly" >}}

- **Aktuální stack frame** je vždy ten, který je "na vrcholu" [^s]
- Když proces přidává stack frame tak se tento nový stack frame stane aktuálním stack framem.
- Když proces odstraní stack frame tak vždz odstraní aktuální stack frame. V ten moment se aktuálním stack framem stane ten pod ním.
- Jakmile dojde k odstranění posledního stack frame tak to znamená, že vlákno dokončilo běh instrukcí a bude ukončeno.

Dále platí, že stack frame **není fixní a jeho obsah může libovolně růst** --- ale jen u **aktuálního stack framu**-

[^l]: *Last In, First Out - poslední uvnitř, první ven*
[^s]: *V bitech samozřejmě žádné "nahoře" nebo "dole" není.*