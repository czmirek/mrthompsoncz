---
draft: false
title: Hradlo a tranzistor
weight: 330
---

Z předchozích kapitol už víte, že pokud signály interpretujeme jako jedničky a nuly tak s nimi můžeme operovat jako s číslicemi ve dvojkové soustavě.

Procesor umí provádět hromadu různých matematických operací: sčítat, odčítat, násobit, dělit atd. apod.

Není nutné vědět, jak jsou v procesoru zadrátované všechny matematické operace, každopádně je dobré mít nějakou základní představu, jak vypadá třeba sečtení dvou čísel.

Než se k tomu dostaneme, je nutné si ještě povědět o 2 dalších věcech a to jsou hradla a tranzistory.

## Co je hradlo?

Hradlo (v angličtině gate) se zakresluje na úrovni digitálního signálu. Je to úplně základní a nejčastější prvek, který se do digitální vrstvy zakresluje.

Co ale přesně hradlo dělá?

No je to v zásadě jednotka digitálního schématu, která na základě vstupních signálů produkuje výstupní signály podle nějaké logiky. Podívejte se na animace níže.

## Základní hradla

**AND hradlo**
![AND hradlo](/jak-se-stat-ajtakem/signalni-vrstva/andhradlo.gif)

**OR hradlo**
![OR hradlo](/jak-se-stat-ajtakem/signalni-vrstva/orhradlo.gif)

**NOT hradlo**
![NOT hradlo](/jak-se-stat-ajtakem/signalni-vrstva/nothradlo.gif)

**XOR hradlo**
![XOR hradlo](/jak-se-stat-ajtakem/signalni-vrstva/xorhradlo.gif)

Základní hradla jsou tato 4.

- **AND**: Pokud je ve všech vstupech signál, pošli signál.
- **OR**: Pokud je v aspoň jednom vstupu signál, pošli signál.
- **NOT**: Výstupní signál je opačný proti vstupnímu signálu
- **XOR**: Výstupní signál je pouze tehdy, pokud počet signálů s hodnotou 1 na vstupu je lichý.

## Další hradla

**NAND hradlo**
![NAND hradlo](/jak-se-stat-ajtakem/signalni-vrstva/nandhradlo.gif)

**NOR hradlo**
![NOR hradlo](/jak-se-stat-ajtakem/signalni-vrstva/norhradlo.gif)

**XNOR hradlo**
![XNOR hradlo](/jak-se-stat-ajtakem/signalni-vrstva/xnorhradlo.gif)

**Zajímavost**: S kombinací NAND hradel lze nasimulovat jakékoliv jiné hradlo

## Co je tranzistor?

Tranzistor je elektronický prvek, ze kterého je hradlo postavené na elektronické vrstvě.

- Tranzistory jsou extrémně levné na výrobu.
- Předání signálu tranzistorem využívá chování elektronů ve dvou různě polovodivých materiálech vedle sebe.
- Procesor obsahuje 50 miliard tranzistorů právě za účelem stavby různých hradel a složitějších rozhodovacích hradlových systémů.
- Toto není návod pro elektrotechniky, pro ajťáka fakt není důležitý vědět, jak jsou tranzistory zapojené a jak přesně fungují takže se tomu věnuji jen v této kapitole.

### Ukázka NAND hradla v elektrickém schématu s tranzistory

jako ajťáka nás elektrická schémata nezajímají ale mám pocit, že je dobré sem dát aspoň ukázku elektrického schématu nějakého hradla, jak vypadá v procesoru. Není důležité tomu schématu rozumět, je ale důležité vědět, že hradla v signální vrstvě jsou implementována tranzistory v elektronické vrstvě.

![CMOS NAND gate](/jak-se-stat-ajtakem/signalni-vrstva/cmosnandgate.webp)

### Moorův zákon

Jakýsi Moore vysledoval, že počet tranzistorů v procesoru se dvojnásobí každé 2 roky při stejné ceně. Není to nijak užitečná informace ale z nějakýho důvodu ajťáci tuhle informaci zbožňujou. Pravda je ale, že od roku 2010 se toto tempo zpomalilo pod úroveň Moorova zákona.

![Moorův zákon](/jak-se-stat-ajtakem/signalni-vrstva/mooreslaw.png)
