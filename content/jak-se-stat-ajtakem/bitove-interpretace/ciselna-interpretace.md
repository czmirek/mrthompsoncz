---
draft: false
title: Číselná interpretace
weight: 7010
description: Jak lze bity používat jako čísla ve dvojkové soustavě a jaký je rozdíl mezi dvojkovou a desítkovou číselnou soustavou
---

Číselná interpretace je pohled na bity jako na čísla.  

## Cifry desítkové soustavy

Kolik používáme běžně **cifer** tzn. znaků, které reprezentují číslici?

Je jich 10. 

Jsou to znaky: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9. Každé číslo vyšší než 9 obsahuje kombinaci předchozích cifer.

- 10 je číslo, které se skládá ze dvou cifer: 1 a 0.
- 4269 je číslo, které se sdkládá ze 4 cifer: 4, 2, 6 a 9.

Jinak řečeno v běžném životě počítáme v **desítkové soustavě**.

## Cifry dvojkové soustavy

Počítače pracují s **bity** které obsahují jen 2 možné hodnoty: 1 a 0.

Z těchto dvou hodnot už můžeme počítat ve **dvojkové soustavě**.

Počítání funguje úplně stejně jako v desítkové soustavě.
- 0
- 1
- 10
- 11
- 100
- 101
- 110
- 111
- 1000
- atd..

## Vztah mezi desítkovou a dvojkovou číselnou soustavou

- **Dvojková soustava** se počítá takto: 0<sub>2</sub>, 1<sub>2</sub>, 10<sub>2</sub> … k číslům se přidává dvojka dole aby bylo jasné, že je to číslo ve dvojkové soustavě.
- **Desítková soustava** se počítá takto: 0<sub>10</sub>, 1<sub>10</sub>, 2<sub>10</sub>…

Nyní se podívejte, jak čísla v desítkové soustavě odpovídají číslům ve dvojkové soustavě.

- 0<sub>10</sub> = 0<sub>2</sub>
- 1<sub>10</sub> = 1<sub>2</sub>
- 2<sub>10</sub> = 10<sub>2</sub>
- 3<sub>10</sub> = 11<sub>2</sub>
- 4<sub>10</sub> = 100<sub>2</sub>
- 5<sub>10</sub> = 101<sub>2</sub>

## Exponenciální řada 2<sup>x</sup>

Většina běžných ajťáků si pamatuje cca prvních 10 čísel z číselné řady 2<sup>x</sup> (2, 4, 8, 16, 32, 64…) protože se tyto hodnoty v IT vyskytují úplně všude.

Podívejte se na následující tabulku.

<pre>
 Dvojková         Desítková  
 číselná          číselná       Odpovídá číslu 2<sub>10</sub>
 soustava         soustava      s exponentem x
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