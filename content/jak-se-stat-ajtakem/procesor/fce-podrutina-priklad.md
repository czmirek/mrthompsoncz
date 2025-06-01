---
draft: true
title: Příklad v instrukcích
weight: 70334
---

Představte si, že programujete napřímo na nějakém studentském procesoru [^f], kde pro sečtení dvou čísel musíte zavolat 3 různé instrukce za sebou: `ADD_A`, `ADD_B`, `ADD_C`. Váš program potřebuje sčítat čísla celkem často a tak je nutné pro sečtení čísel napsat funkci.

{{< figure align=center width=700 src="../fx_instrukce.png" title="Příklad funkce v instrukcích" >}}

- Na začátku programu přeskočíme samotnou funkci, program začíná na adrese `0x09`
- Na adrese `0xC8` potřebujeme sečíst 2 čísla, která máme připravené na adresách `0xEA` a `0xEB`.
  - `[0xEA]: 00000011` = 3
  - `[0xEB]: 00000100` = 4
- Číslo z adresy `0xEA` uložíme na adresu `0x01` což je první parametr sčítací funkce.
- Číslo z adresy `0xEB` uložíme na adresu `0x02` což je druhý parametr sčítací funkce.
- Ze sčítací funkce se ale musíme pak dostat zpět. Sčítací funkci tedy ještě sdělíme, že po uložení výsledku musí pokračovat na adrese `0xCB`.

[^f]: *Toto je pouze vymyšlený příklad. Jak se funkce/podrutiny v moderních počítačích tvoří se dozvíte v následujících kapitolách.*
