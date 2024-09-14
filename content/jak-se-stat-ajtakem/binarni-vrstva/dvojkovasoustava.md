---
draft: false
title: Dvojková soustava
weight: 802
---

Počítejte na prstech jako v první třídě: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10. Kolik obsahuje desítková soustava **cifer** tzn. znaků, které reprezentují číslici?

Je jich 10. Jsou to znaky: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9. Každé číslo vyšší než 9 obsahuje kombinaci předchozích cifer.

- 10 je číslo, které se skládá ze dvou cifer: 1 a 0.
- 6969 je číslo, které se sdkládá ze 4 cifer: 6, 9, 6 a 9.
- A tak dále.

Teď si představte, že počítáte na prstech ale máte jen jednu ruku a jeden prst. Máte k dispozici jen 2 cifry: 0 a 1. Jak se počítá s čísly, když jsou k dispozici jen 2 cifry? Úplně stejně. 

0, 1, 10, 11, 100, 101, 110, 111, 1000... — blahopřeji, právě jste se naučili počítat ve dvojkové soustavě.

## Vztah mezi desítkovou a dvojkovou číselnou soustavou

- Dvojková soustava se počítá takto: 0<sub>2</sub>, 1<sub>2</sub>, 10<sub>2</sub> … k číslům se přidává taková dvojka dole aby bylo jasné, že je to číslo ve dvojkové soustavě.
- Desítková soustava se počítá takto: 0<sub>10</sub>, 1<sub>10</sub>, 2<sub>10</sub>…

Otázka: kolik je číslo 10<sub>2</sub> v desítkové číselné soustavě?
Správně: je to číslo 2<sub>10</sub>!

Podívejte se na následující číselnou řadu, jak číslo v desítkové soustavě odpovídá číslům ve dvojkové soustavě a začne to být jasné.

- 0<sub>10</sub> = 0<sub>2</sub>
- 1<sub>10</sub> = 1<sub>2</sub>
- 2<sub>10</sub> = 10<sub>2</sub>
- 3<sub>10</sub> = 11<sub>2</sub>
- 4<sub>10</sub> = 100<sub>2</sub>
- 5<sub>10</sub> = 101<sub>2</sub>

Následující hodnoty z desítkové číselné soustavy (2, 4, 8, 16, 32, 64… ) zná většina běžných akťáků nazpaměť protože se tyto hodnoty v IT vyskytují úplně všude. Počítače jsou z povahy věci *dvojkové*.

<pre>
 Dvojková         Desítková  
 číselná          číselná       Odpovídá číslu 210
 soustava         soustava      s exponentem
 --------------------------------------------------
 1                1             2<sup>0</sup>
 10               2             2<sup>1</sup>
 100              4             2<sup>2</sup>
 1000             8             2<sup>3</sup>
 10000            16            2<sup>4</sup>
 100000           32            2<sup>5</sup>
 1000000          64            2<sup>6</sup>
 10000000         128           2<sup>7</sup>
 100000000        256           2<sup>8</sup>
 1000000000       512           2<sup>9</sup>
 10000000000      1024          2<sup>10</sup>
 100000000000     2048          2<sup>11</sup>
 1000000000000    4096          2<sup>12</sup>
 (dále jsou zajímavé už jen tyto hodnoty)
 ...              65536         2<sup>16</sup>
 ...              ...           2<sup>32</sup>
 ...              ...           2<sup>64</sup>
 
</pre>