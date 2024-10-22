---
draft: false
title: Funkce / podrutina 2
weight: 70331
---

V minulém díle jsem pojmenoval, co je [funkce / podrutina]({{< relref "fce-podrutina" >}}) a ukázal jsem, jak taková podrutina může být vyrobena díky `JUMP` instrukci.

Tvůrci softwaru už dávno přišli na to, že je mnohem lepší pracovat s konceptem funkcí které mají **vstupní a výstupní parametry**.

## Příklad

Funkci si lze představit jako nějaký stroj. Když do něj nasypete tak podle toho něco vyprodukuje. 

{{< figure align=center width=200 src="../fx.png" title="Matematická funkce. Zdroj: Wikipedia" >}}

Jednoduchým příkladem je funkce **SEČTI** která má 2 vstupní parametry - první sčítanec, druhý sčítanec - a 1 výstupní parametr - součet. Zápis funkce s dosazenými hodnotami vypadá takto:

> `7 = SEČTI(3, 4)`

Jak sami vidíte, je to jenom takový jiný, divný zápis pro `3 + 4 = 7`. Když *"zavoláte"* funkci SEČTI a použijete čísla 3 a 4 jako vstupní parametry tak vám vždy *"vrátí"* výsledek 7 bez ohledu na to, kolikrát funkci *"zavoláte"*.