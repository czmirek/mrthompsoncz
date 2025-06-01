---
draft: false
title: Funkce / podrutina 2
weight: 70331
---

<div class="note-blue">

⚠️ Koncept funkcí je v IT extrémně důležitý a objevuje se úplně všude.

- Pro stisknutí tlačítka na klávesnici se spustila nějaká funkce
- Při načtení webové stránky v prohlížeči se spustila nějaká funkce
- Při ztučnění písma ve Wordu se spustila nějaká funkce
- atd.

V následujících 2 kapitolách se věnuji funkcím víc dopodrobna.

</div>

V minulém díle jsem pojmenoval, co je [funkce / podrutina]({{< relref "fce-podrutina" >}}) a ukázal jsem, jak taková podrutina může být vyrobena díky `JUMP` instrukci.

## Příklad

Funkci si lze představit jako nějaký stroj. Když do něj něco nasypete tak podle toho něco vyprodukuje.

{{< figure align=center width=200 src="../fx.png" title="Matematická funkce. Zdroj: Wikipedia" >}}

Jednoduchým příkladem je funkce **SEČTI** která má 2 vstupní parametry - první sčítanec, druhý sčítanec - a 1 výstupní parametr - součet. Zápis funkce s dosazenými hodnotami vypadá takto:

> `7 = SEČTI(3, 4)`

Jak sami vidíte, je to jenom takový jiný, divný zápis pro `3 + 4 = 7`. Když *"zavoláte"* funkci SEČTI a použijete čísla 3 a 4 jako vstupní parametry tak vám vždy *"vrátí"* výsledek 7 bez ohledu na to, kolikrát funkci *"zavoláte"*.