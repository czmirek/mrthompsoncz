---
draft: false
title: Multithreading
weight: 200300
---

Řekněme, že máme k dispozici jednojádrový procesor. Běžný OS na takovém procesoru stále dokáže rozeběhnout více programů najednou a to díky mechanismu kterému se říká **multithreading**.

## Přirovnání ke koncertu vojenských kapel

Představte si, že jste organizátor koncertu s jedním pódiem. Na tomto koncertu musí vystoupit 10 kapel.

V těchto kapelách hrají jenom vojáci kteří vás poslouchají na slovo, protože jste jejich šílený velitel. 

Můžete jakoukoliv kapelu kdykoliv přerušit a vyměnit za jinou kapelu i uprostřed písničky. V ten moment se však musí kapela na pódiu sebrat a vypadnout a uvolnit místo jiné kapele, která tam musí naběhnout, připravit si nástroje a pak začít hrát.

Takový koncert by pravděpodobně za moc nestál ale o to tady nejde.

## Multithreading

Multithreading je přesně tento proces, který umí všechny běžné OS.

**Čas procesoru je každému programu přidělován**.  

Procesu který organizuje kdy který program bude běžet se v OS říká **scheduler** [^1]. Operace přepnutí mezi přidělením času z jednoho na druhý program se říká **context switch** [^2].

Toto znamená, že **souběžný běh programů je vlastně jen na oko**. Procesory pořád zpracovávají instrukce za sebou.

Moderní procesory jsou však tak extrémně rychlé, že to v praxi vypadá, jako by umožňovaly souběžný běh více programů najednou.

<div style="background-color:white;color:black;">
{{< figure align=center width=300 src="https://upload.wikimedia.org/wikipedia/commons/a/a5/Multithreaded_process.svg" >}}
</div>

*Zdroj: [Wikipedia](https://en.wikipedia.org/wiki/Multithreading_(computer_architecture))*

## Jak pracuje scheduler?

Scheduler **balancuje** čas procesoru mezi všemi běžícími programy. Jak přesně toto balancování dělá je pro běžného ajťáka nepodstatný detail. Každé OS toto dělá jinak a navíc jde o mnohem komplexnější úlohu, než se zdá.

Scheduler toto balancování rozhoduje:

- podle počtu jader na procesoru
- podle aktuálního počtu běžících programů
- podle aktuálních i historických statistik které si o běžících programech udržuje
- podle uživatelem nastavených uživatelských priorit [^4]
- podle uživatelem nastavených jader [^5]
- atd.

## Context switch

Context switch, jak už bylo řečeno, je proces přepnutí mezi přidělením času procesorového jádra z jednoho programu na jiný program. Tento proces, přestože není jednoduchý, je v moderních procesorech **extrémně rychlý** a v průměru trvá v řádech mikrosekund.

[^1]: *V přirovnání výše to byl šílený velitel*  
[^2]: *V přirovnání výše to je proces výměny jedné kapely za druhou*.
[^3]: *1 mikrosekunda = 1 miliontina sekundy*
[^4]: *Přestože moderní OS umožňují uživatelům přidělovat běžícím programům jakési priority tak to není běžná praxe jak mezi běžnými uživateli tak i mezi běžnými ajťáky.*
[^5]: *OS umožňují uživatelům určit, na jakém procesorovém jádře mají jednotlivé programy běžet. Stejně jako výše, není to běžná praxe.*
