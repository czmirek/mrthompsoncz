---
draft: false
title: Složitosti kterým nemusíme rozumět
weight: 70900
---

## Cache

RAM pamět byla historicky pomalejší než procesor.

Z tohoto důvodu obsahují procesory řadu svých vlastních miniaturních pamětí zvaných *cache* jejichž kapacita bývá jen pár megabajtů. Tyto paměti jsou odstupňované od nejrychlejší (L1) po nejpomalejší (až L4) a tyto *cache* mohou být v procesoru vyrobeny i za použití jiné výrobní technologie.

Synchronizace mezi RAM pamětí a procesorem tak probíhá i prostřednictvím těchto cache. Tyto synchronizace jsou celkem komplikované a hlavně probíhají už na hardwarové úrovni (tzn. už je to tak "zadrátované").

## Registry

Instrukce pracují s **registry** což jsou opravdu malé paměti s kapacitou jen třeba 4 bajty. 

Když chcete např. sečíst dvě čísla tak instrukce vašeho programu mají zpravidla tuto posloupnost:

- Ulož hodnotu do registru A
- Ulož hodnotu do registru B
- Sečti dvě čísla `[Registr A]` + `[Registr B]`
  
Instrukce sečtení uložila výsledek do registru C.

V moderních procesorech je těchto registrů z historických důvodů obrovské množství a jejich použití je napříč instrukcemi nekonzistentní. V rámci tohoto návodu se však registry zabývat nepotřebujeme.

## Pipelines

V moderních procesorech se instrukce zpracovávají v rámci **pipeline** která instrukce zpracovává v několika krocích. Počet těchto kroků se liší mezi procesory, u některých se uvádí 5 až 10, u jiných klidně až 50.

Každý krok může vyžadovat různé množství cyklů pro zpracování.

{{< figure align=center width=300 src="../pipeline.png" title="Cyklus procesoru" >}}

## Superskalární architektura

Moderní procesory jsou zároveň schopné **v rámci jednoho procesorového jádra** reálně zpracovávat **některé** instrukce paralelně. Během jednoho cyklu je tak procesor schopný z instrukčního toku zpracovat více než 1 instrukci najednou.

Nejde o "skutečnou" paralelitu jako v případě dvou a více procesorových jader. Moderní CPU jednoduše dokáže rozlišit, že některé instrukce z instrukčního toku lze spustit najednou aniž by to ovlivnilo výsledek. 

## Optimalizace pořadí instrukcí [^o]

Instrukce tečou do procesoru v pořadí, jedna za druhou. Moderní CPU se však tímto pořadím nutně neřídí. 

Moderní CPU je schopné detekovat, že aktuálně probíhající instrukce čekají na nějaká data a další čekání by mohlo vést k vyplýtvaným CPU cyklům. Místo toho se tedy CPU rozhodne, že bude pokračovat v instrukcích, které už na žádná data čekat nemusí.

Samozřejmě to nesmí ovlivnit celkový výsledek --- CPU toto provádí jen pokud si je 100% jisté, že si toto "přeskakování" může dovolit a výsledek zůstane stejný.

## Prediktivní mechanismy

Moderní procesory si ukládají krátkodobou statistiku nejpoužívanějších instrukcí a jejich výsledků. Při zpracování instrukcí se snaží odhadnout výsledek pro ušetření velkého množství cyklů a zpracování dalších instrukcí.

V nějaký moment si však musí ověřit, že skutečný výsledek je totožný s predikcí. Pokud predikce selže, musí se CPU vrátit o několik kroků zpátky a všechny instrukce se musí provést v jednotlivých krocích řádně, bez použití prediktivních kroků.

Běžný uživatel si toho nevšimne. K selhání CPU predikcí dochází ve vašem běžném počítači každou chvíli. Poměr úspěšných predikcí je však v běžném provozu vysoký a proto se výrobcům CPU vyplatí takové prediktivní systémy do CPU zabudovávat.

## Variabilní délka instrukce

U moderních CPU mají instrukce proměnlivou délku. U `x86` to je mezi 8 až 120 bity (nebo 1 až 15 bajty).

CPU v jednom cyklu nejdřív detekuje typ instrukce podle kterého zjistí, jakou délku tato instrukce může mít a v dalších cyklech (v rámci pipelajny, viz. výše) se pustí do dekódování zbytku instrukce. 

## Buffery

Každá komponenta v počítači běží pod určitou rychlostí. Architektura moderního počítače obsahuje obrovské množství různých pomocných obvodů a čipů, nebo "*bufferů*" které slouží právě k dočasnému uložení dat mezi komponentami, které pracují na různých rychlostech. To se odvíjí i od **chipsetu základní desky**.

Každý výrobce však k tomu může mít jiný přístup.

- Každá základní deska může obsahovat úplně jiné uspořádání čipů/bufferů
- Každá komponenta může obsahovat úplně jiné uspořádání čipů/bufferů
- Každý procesor může obsahovat úplně jiné uspořádání cache, registrů a odlišné chování pipeline.

Realita, jak a kudy tečou v moderních počítačích konkrétní bity, by se lépe dala znázornit následujícím obrázkem.

{{< figure align=center src="../hwcmp.png" title="Hardwarové složitosti, které lze ignorovat" >}}

<div class="note-blue">

⚠️ **Důležité k zapamatování**: Pointa této kapitoly je, že pro běžného ajťáka není důležité se těmito detaily do hloubky zabývat. Je dobré vědět, že existují, ale běžný ajťák na tento problém nenarazí. [^x]

</div>

[^o]: *Z angličtiny "out-of-order execution"*

[^x]: *Snad kromě člověka, který v [nejpopulárnější otázce na Stackoverflow](https://stackoverflow.com/questions/11227809/why-is-processing-a-sorted-array-faster-than-processing-an-unsorted-array) řešil problém způsobený právě prediktivními mechanismy CPU.*