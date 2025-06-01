---
draft: false
title: Idle task
weight: 200350
---

V minulém díle jsem řekl, že scheduler **balancuje** čas procesoru mezi všemi běžícími programy. 

Co ale OS dělá, když jsou všechny instrukce **splněny včas** a už nejsou žádné instrukce, které by mohly v procesoru běžet? Nezapomeňte na to, že pokud by procesoru instrukce došly, počítač by se nejspíš vypnul nebo restartoval.

 V tom případě procesor přidělí čas procesoru jedné své vlastní speciální úloze, které se říká **idle task**.

**Idle task** reálně **nic nedělá** a toto "nicnedělání" dělá do nekonečna. Tato úloha má nejnižší možnou prioritu a jejím účelem je zaplnit procesor nějakými "nicnedělajícími" instrukcemi do té doby, dokud nenastane čas pro zpracování instrukcí pro další proces. Toto balancování probíhá každou chvíli, v mikrosekundových intervalech!

## Instrukce pro "nicnedělání"

Jedna z procesorových instrukcí, kterou idle task úlohy mohou využívat, je `NOP` instrukce, kterou jsem [již popisoval]({{< relref "../procesor/nop" >}}). Účelem této instrukce je právě nic nedělat a OS ji mohou využít v případě, kdy veškeré ostatní procesy již byly zpracovány.

U moderních procesorů se však využívají specializované instrukce `HALT` nebo `MWAIT` které jsou schopné procesor pozastavit - nebo dokonce jej přepnout do nějakého "úsporného režimu" [^u] - na krátký časový interval nebo do té doby, dokud procesor nezaznamená signál pro přerušení (ať už hardwarový nebo softwarový) nebo jinou událost jako zápis do paměti a podobně.

[^u]: *To není totéž, jako když přepnete PC do úsporného režimu. V takovém případě je procesor reálně vypnutý ale základní deska je zapnutá a hlídá, jestli jste třeba nepohli myší, nezmáčkli klávesu na klávesnici a podobně.*