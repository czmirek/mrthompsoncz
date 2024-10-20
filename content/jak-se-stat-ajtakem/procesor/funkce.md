---
draft: false
title: 'Úplná funkce'
weight: 70331
---

V minulém díle jsem pojmenoval, co je [podrutina]({{< relref "ridici-instrukce-2" >}}) a ukázal jsem, jak taková podrutina může být vyrobena díky `JUMP` instrukci.

Tvůrci softwaru už dávno přišli na to, že je mnohem lepší pracovat s konceptem **matematických funkcí** které mají **vstupní a výstupní parametry**.

## Co je matematická funkce?

Matematickou funkci si lze představit jako nějaký stroj. Když do něj něco nasypete tak podle toho něco vyprodukuje. 

{{< figure align=center width=200 src="../fx.png" title="Matematická funkce. Zdroj: Wikipedia" >}}

Matematická funkce se chová pořád stejně. To znamená, že pokud do stroje dvakrát za sebou nasypete jedno a totéž tak ten stroj vám vyprodukuje dvakrát totéž. 

Jednoduchým příkladem je funkce **SEČTI** která má 2 vstupní parametry - první sčítanec, druhý sčítanec - a 1 výstupní parametr - součet. 

Zápis funkce s dosazenými hodnotami vypadá takto:

> `7 = SEČTI(3, 4)`

Jak sami vidíte, je to jenom takový jiný zápis pro `3 + 4 = 7`. Když použijete čísla 3 a 4 tak výsledek vždy bude 7.

## Jak udělat funkci v instrukcích pro procesor [^f]

Představte si, že se nacházíte na nějakém studentském procesoru, kde pro sečtení dvou čísel musíte zavolat 3 různé instrukce za sebou: `ADD_A`, `ADD_B`, `ADD_C`. Váš program potřebuje sčítat čísla celkem často a tak je nutné pro sečtení čísel napsat funkci.

{{< figure align=center width=700 src="../fx_instrukce.png" title="Příklad funkce v instrukcích" >}}

- Na začátku programu přeskočíme samotnou funkci, program začíná na adrese `0x09`
- Na adrese `0xC8` potřebujeme sečíst 2 čísla, která máme připravené na adresách `0xEA` a `0xEB`.
  - `[0xEA]: 00000011` = 3
  - `[0xEB]: 00000100` = 4
- Číslo z adresy `0xEA` uložíme na adresu `0x01` což je první parametr sčítací funkce.
- Číslo z adresy `0xEB` uložíme na adresu `0x02` což je druhý parametr sčítací funkce.
- Ze sčítací funkce se ale musíme pak dostat zpět. Sčítací funkci tedy ještě sdělíme, že po uložení výsledku musí pokračovat na adrese `0xCB`.

[^f]: *Toto je pouze vymyšlený příklad. Jak se funkce reálně v procesorech implementují se dozvíte v následující kapitole.*