---
draft: false
title: Hardwarové přerušení
weight: 70339
---

Jak už víte z předchozích kapitol, procesor zpracovává instrukce **sériově, tedy za sebou, jednu po druhé**. Procesor v rámci *pipeline* je sice schopný zpracovávat instrukce v různých krocích, může v rámci této pipeline přeskakovat zbytečné instrukce či predikovat jejich výsledek, každopádně pořád platí to, že procesor v každém tomto kroce zpracovává právě pouze jednu instrukci.

Kdyby však toto bylo vše, co procesor umí, tak bychom s počítači zůstávali někde v dávné historii. Stále bychom používali počítače tím způsobem, že bychom jim museli nejdřív zadat seznam instrukcí, pak je spustit a počkat na výsledek.

## Vstupy a výstupy (neboli I/O)

Řekněme, že zmáčknete tlačítko na klávesnici nebo pohnete myší.

Tato informace se nějakým způsobem musí dostat do procesoru, protože procesor je zodpovědný za to, že dá této vaší akci nějaký význam. Když pohnete myší, procesor je zodpovědný za to, že se pohne kurzor na vašem monitoru. [^s]

Kdyby procesor četl připravené instrukce od začátku do konce tak by nebyl schopný reagovat na požadavky odeslané z klávesnice nebo z myši.

## Přerušení, anglicky *interrupt*

Z toho důvodu jsou procesory schopné zpracovávat *přerušení* - v tomto případě jde o **hardwarové přerušení**.

Toto přerušení je jednoduše instrukce která se na základě **nějakého signálu z komponenty** sama vecpe do toku instrukcí, které procesor právě zpracovává.

{{< figure align=center width=500 src="../interrupt1.png" title="Přerušení - krok 1" >}}

Přerušení v sobě nese jakýsi identifikátor označující hardwarové přerušení. CPU se podle tohoto identifikátoru podívá do speciální tabulky [^t] která obsahuje dva sloupce: identifikátor a adresa v RAM paměti na [funkci/rutinu]({{< relref "ridici-instrukce-2" >}}), která se má v případě přerušení zpracovat.

{{< figure align=center width=500 src="../interrupt2.png" title="Přerušení - krok 2" >}}

Jakmile je funkce/rutina zpracována tak tok instrukcí pokračuje tam, kde skončil před přerušením. 

{{< figure align=center width=500 src="../interrupt3.png" title="Přerušení - krok 3" >}}

Pohybování kurzorem po obrazovce generuje klidně stovky přerušení za vteřinu a každé toto přerušení znamená pohyb kurzoru myši z jednoho místa na obrazovce na jiné místo na obrazovce.

[^s]: *Kurzor není nic jiného, než jen pár světélek (pixelů) na vašem monitoru.*
[^n]: *Jednoduchým příkladem je signál z klávesnice nebo myši.* 
[^t]: *IDT - Interrupt Descriptor Table*