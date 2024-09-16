---
draft: false
title: Přerušení
weight: 711
---

Jak už víte z předchozích kapitol, procesor zpracovává instrukce **sériově, tedy za sebou, jednu po druhé**. Procesor v rámci *pipeline* je sice schopný zpracovávat instrukce v různých krocích, může v rámci této pipeline přeskakovat zbytečné instrukce či predikovat jejich výsledek, každopádně pořád platí to, že procesor v každém tomto kroce zpracovává právě pouze jednu instrukci.

Kdyby však toto bylo vše, co procesor umí, tak bychom s počítači zůstávali někde v dávné historii. Stále bychom používali počítače tím způsobem, že bychom jim museli nejdřív zadat seznam instrukcí, pak je spustit a počkat na výsledek.

## Vstupy a výstupy (neboli I/O)

Řekněme, že zmáčknete tlačítko na klávesnici nebo pohnete myší.

Tato informace se nějakým způsobem musí dostat do procesoru, protože procesor je zodpovědný za to, že dá této vaší akci nějaký význam. Když pohnete myší, procesor je zodpovědný za to, že se pohne kurzor na vašem monitoru. [^s]

Kdyby procesor četl připravené instrukce od začátku do konce tak by nebyl schopný reagovat na požadavky odeslané z klávesnice nebo z myši.

## Přerušení, anglicky *interrupt*

Z toho důvodu jsou procesory schopné zpracovávat *přerušení*.

Toto přerušení je jednoduše instrukce která se na základě **nějaké události** [^n] sama vecpe do toku instrukcí, které procesor právě zpracovává.


{{< figure align=center width=500 src="../interrupt1.png" title="Přerušení - krok 1" >}}

Tato instrukce přerušení v sobě obsahuje nějakou adresu. Pokud procesor tuto adresu zná (tzn. byl mu dodaný nějakými instrukcemi předem) tak spustí instrukce, na které se na této adrese nachází, **od začátku až do konce**. 

{{< figure align=center width=500 src="../interrupt2.png" title="Přerušení - krok 2" >}}

Jakmile zpracuje všechny instrukce až do konce tak se vrátí k původním instrukcím, které procesor zpracovával před přerušením. 

{{< figure align=center width=500 src="../interrupt3.png" title="Přerušení - krok 3" >}}

[^s]: Kurzor není nic jiného, než jen pár světélek (pixelů) na vašem monitoru.
[^n]: Jednoduchým příkladem je signál z klávesnice nebo myši. Komplikovanější příklad je signál na základě jiné instrukce, o tom budu však mluvit později. 