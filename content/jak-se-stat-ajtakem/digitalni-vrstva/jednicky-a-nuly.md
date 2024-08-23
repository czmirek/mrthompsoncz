---
draft: true
title: Jedničky a nuly
weight: 510
---


## Dvojková soustava

Další „vrstva“ nebo „pohled“ který teď přidám je binární aritmetika.

- Tam, kde není signál, tam je číslice 0
- Tam, kde je signál, tam je číslice 1

![Binární aritmetika](/jak-se-stat-ajtakem/signalni-vrstva/binaritmetika.png)

Číslo 1 nebo 0 se v IT nazývá bit a umožňuje počítat ve dvojkové soustavě.

To už zní možná dost šíleně. Co je dvojková soustava?

Je to jednoduché. Počítejte na prstech jako v první třídě.

0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10.

Kolik máš prstů? 10! Výborně! Tady máš bombónek! 🍬

Kolik obsahuje desítková soustava cifer (znak, který reprezentuje číslici)?
Také 10. Jsou to znaky: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9.

10 je číslo, které se skládá ze dvou cifer: 1 a 0.
6969 je číslo, které se sdkládá ze 4 cifer: 6, 9, 6 a 9.
A tak dále.

No a teď si představ, že máš jen jednu ruku a na jedné ruce jen jeden prst.

Máš k dispozici jen 2 cifry: 0 a 1. Jak se počítá s čísly, když jsou k dispozici jen 2 cifry? Úplně stejně. Pro většinu lidí co se nevyzná v IT to vypadá strašně nezvykle.

0, 1, 10, 11, 100, 101, 110, 111, 1000… — blahopřeji, právě jste se naučili počítat ve dvojkové soustavě.

Fakt za tím nehledej žádnou vědu. Funguje to úplně stejně jako kdybys měl 10 prstů. Jakmile dopočítáš do 9 tak prostě vezmeš cifry 1 a 0 a dáš je vedle sebe a máš číslo 10.

Ve dvojkové soustavě uděláš úplně totéž – 0, 1, 10. 

## Vztah mezi desítkovou a dvojkovou číselnou soustavou


- Dvojková soustava se počítá takto: 0<sub>2</sub>, 1<sub>2</sub>, 10<sub>2</sub> … k číslům se přidává taková dvojka dole aby bylo jasné, že je to číslo ve dvojkové soustavě.
- Desítková soustava se počítá takto: 0<sub>10</sub>, 1<sub>10</sub>, 2<sub>10</sub>…

Otázka za 2 bludišťáky: kolik je číslo 10<sub>2</sub> v desítkové číselné soustavě?
Správně: je to číslo 2<sub>10</sub>!

Podívejte se na následující číselnou řadu, jak číslo v desítkové soustavě odpovídá číslům ve dvojkové soustavě a začne vám to být jasné.

- 0<sub>10</sub> = 0<sub>2</sub>
- 1<sub>10</sub> = 1<sub>2</sub>
- 2<sub>10</sub> = 10<sub>2</sub>
- 3<sub>10</sub> = 11<sub>2</sub>
- 4<sub>10</sub> = 100<sub>2</sub>
- 5<sub>10</sub> = 101<sub>2</sub>

Následující hodnoty z desítkové číselné soustavy (2, 4, 8, 16, 32, 64… ) zná většina ajťáků zpaměti, protože se v IT vyskytují úplně všude. Počítače jsou z povahy věci „dvojkové“ (je signál/není signál).
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

Ajťáci ještě chápou důležitost této číselné řady: 2<sup>8</sup>, 2<sup>16</sup>, 2<sup>32</sup>, 2<sup>64</sup>, 2<sup>128</sup>, 2<sup>256</sup>, 2<sup>512</sup>. Tato řada se často objevuje v IT kryptografii.

Podobně jako vás na základní škole učili postup násobení nebo dělení velkých čísel na papíře tak existuje postup na převod čísel mezi různými číselnými soustavami. V tomto návodu pro laiky to ale není podstatné. Myslím si, že většina ajťáků se postup převodu mezi číselnými soustavami naučila pouze jednou ve škole a od té doby to zapomněli a v případě potřeby použijí kalkulačku, která to umí.

## Další číselné soustavy vyskytující se v IT

### 16: šestnáctková (hexadecimální) číselná soustava

V IT se běžně pracuje s čísly v šestnáctkové soustavě. Tato soustava obsahuje následující cifry: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F.

Počítá se následovně: 0, 1, …, 9, A, B, C, D, E, F, 10, 11, 12, 13 … 19, 1A, 1B, 1C, 1D, 1E, 1F, 20, 21.

Z hlavy vytáhnu pouze tuto číselnou řadu:

- F<sub>16</sub> = 15<sub>10</sub>
- FF<sub>16</sub> = 255<sub>10</sub>
- FFFF<sub>16</sub> = 65535<sub>10</sub>

Ajťák kterej si z hlavy pamatuje nějakou dělší číselnou řadu s hexadecimálními čísly to buď fakt k něčemu potřebuje nebo je to prostě jen magor.

### 8: osmičková číselná soustava

Z hlavy dokážu říct, že se tato číselná soustava používá v Linuxu u vyjádření práv pro čtení a zápis v souborech.

Žádnou zajímavou číselnou řadu s osmičkovými čísly jsem si nikdy nezapamatoval.

### 64: šedesátičtyřková soustava

Tato soustava se používá velmi často pro jednoduchou kompresi dat (kolektivně se těmto operacím říká base64). Nedokážu si představit žádnýho ajťáka, který by chtěl s touto šílenou číselnou soustavou něco kloudnýho počítat nebo by si pamatoval všechny znaky které jsou v této řadě obsažené.

## Shrnutí

- Počítače něco počítají úplně ve všech činnostech, které s počítačem provádíme.
- Na signály se nyní koukáme jako na cifry „0“ a „1“ ve dvojkové číselné soustavě
- Díky cifrám 0 a 1 nyní můžeme počítat ve dvojkové soustavě!
- V IT se dále běžně vyskytuje 16, zřídka 8. Pro kompresi dat se často používá 64 číselná soustava.
