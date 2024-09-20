---
draft: false
title: Desetinná čísla
weight: 80080
---

Desetinná čísla znáte. Víte, že `5 / 2 = 2,5`

Jak se s číslem `2,5` pracuje v počítači?

## Desetinná čísla ve dvojkové soustavě

Dokážete odhadnout, kolik je 0,12 v desítkové soustavě?

- 0,1<sub>2</sub> = 0,5<sub>10</sub>
- 0,01<sub>2</sub> = 0,25<sub>10</sub>
- 0,001<sub>2</sub> = 0,125<sub>10</sub>
- 0,0001<sub>2</sub> = 0,0625<sub>10</sub>
- …

Z této číselné řady se dá na první pohled vyčíst jednoduchý vztah vydělením dvěmi.

- 1 / 2 = 0,5
- 0,5 / 2 = 0,25
- 0,25 / 2 = 0,125
- 0,125 / 2 = 0,0625.
- …

Ale co když začnete převádět libovolná čísla z desítkové soustavy do dvojkové soustavy? Pak to začne bejt divný.

1<sub>10</sub> = 1<sub>2</sub>  
0,9<sub>10</sub> = 0,1110011001100110011…<sub>2</sub>  
0,8<sub>10</sub> = 0,11001100110011001101…<sub>2</sub>  
0,7<sub>10</sub> = 0,10110011001100110011…<sub>2</sub>  
0,6<sub>10</sub> = 0,1001100110011001101…<sub>2</sub>  
0,5<sub>10</sub> = 0,1<sub>2</sub>  
0,51<sub>10</sub> = 0,1000001010001111011…<sub>2</sub>  

Většina desetinných čísel z desítkové soustavy nemá ve dvojkové číselné soustavě žádnou hezkou hodnotu a obsahují řadu cifer která se v nějakém složení opakují do nekončena.

Je to stejné, jako `10 / 3 = 3,333333…`

## Počítače neumí být přesné v desetinné interpretaci

⚠️ Pozor na to: většina desetinných čísel desítkové soustavy mají ve dvojkové soustavě hodnoty, jejichž cifry se táhnou do nekonečna ale počítače nemají schopnost uložit nekonečně veliké ani nekonečně přesné číslo.

Co to znamená?

Pokud například pracujete v počítači s číslem 0,8<sub>10</sub> tak musíte počítat s tím, že jeho vyjádření v počítači není přesné protože místo `0,11001100110011001100110011001100....` se uloží například jen `0,1100110011001100`.

Jakmile tuto binární hodnotu převedete zpátky tak nedostanete 0,8<sub>10</sub> ale něco jako **0.799999998779…<sub>10</sub>**