---
draft: false
title: Aritmeticko-logické instrukce
weight: 70310
description: Aritmeticko-logické instrukce
---

Dalšími typy instrukcí jsou aritmeticko-logické instrukce.

## Aritmetické funkce 

Mezi aritmetické (matematické) instrukce patří například:
- sčítání (viz. [Sčítačka]({{< relref "../hradlova-vrstva/scitacka" >}}))
- odčítání
- násobení
- dělení

Tyto instrukce provádějí operace nad dvojkovou soustavou. Z kapitoly o [celých číslech]({{< relref "../bitove-interpretace/cela-cisla" >}}) už víte, že čísla ve dvojkové soustavě lze normálně převést do desítkové soustavy.

<div class="note-blue">

Matematické operace ve dvojkové soustavě dávají stejný výsledek, jako v desítkové soustavě.

5<sub>10</sub> + 7<sub>10</sub> = 12<sub>10</sub> je totéž jako 101<sub>2</sub> + 111<sub>2</sub> = 1100<sub>2</sub>

</div>

Moderní procesory umí stovky dalších matematických funkcí (na dvojkové soustavě) např. pro práci s desetinnými čísly, s vektory a podobně.

## Logické funkce

Mezi logické funkce patří:

- **AND**: všechny hodnoty musí být 1 aby výsledek byl 1, jinak je výsledek 0
- **OR**: aspoň jedna hodnota musí být 1 aby výsledek byl 1, jinak je výsledek 0
- **NOT**: hodnota je převedena na opačnou hodnotu
- **XOR**: výsledek je 1 pokud počet vstupních hodnot, které mají 1, je lichý
- **NAND**: kombinace NOT a AND
- **NOR**: kombinace NOT a OR

**NOT** operace lze provádět nad jediným bitem. Všechny ostatní operace se musí provádět minimálně mezi dvěma různými bity.

### Vyřešené příklady na ukázku

```
NOT 0             = 1
NOT 1111          = 0000
1 AND 1           = 1
1 AND 0           = 0
0 OR 0            = 0
0 OR 1            = 1
1101 AND 1001     = 1001
1101 OR  1001     = 1101
```

## Matematické vlastnosti dvojkových čísel

<div class="note-blue">

⚠️ **Důležité k zapamatování**: Většina běžných ajťáků nejsou bůhví jací matematici.

Je však důležité si pamatovat, že každá matematická operace v počítači lze provést kombinací logických funkcí - viz. [sčítačka]({{< relref "../hradlova-vrstva/scitacka" >}})

Logické instrukce jsou v procesorech nejrychlejší a zabírají nejmenší počet cyklů. Jakým způsobem lze matematické funkce převést čistě do logických není pro běžného ajťáka podstatné.

</div>