---
draft: false
title: Hardwarové přerušení
weight: 70339
description: Jak procesor dostane signál z vnějšího světa?
---

Jak už víte z předchozích kapitol, procesor zpracovává instrukce **sériově, tedy za sebou, jednu po druhé**.

Kdyby však toto bylo vše, co procesor umí, tak bychom stále používali počítače stejným způsobem jako v dávné minulosti - museli bychom nejdřív napsat program, ten spustit a počkat na výsledek. Neměli bychom možnost změnit chování počítače za běhu.

## Přerušení, anglicky *interrupt*

Řekněme, že zmáčknete tlačítko na klávesnici nebo pohnete myší.

V ten moment dojde se signál z myši dostane až do procesoru prostřednictvím mechanismu, kterému se říká **přerušení** [^i]  - v tomto případě jde o **hardwarové přerušení**.

Přerušení je instrukce, která se "vecpe" do toku instrukcí, které procesor právě zpracovává.

{{< figure align=center width=500 src="../interrupt1.png" title="Přerušení - krok 1" >}}

Přerušení v sobě nese jakýsi identifikátor označující hardwarové přerušení. CPU se podle tohoto identifikátoru podívá do speciální tabulky [^t] která obsahuje dva sloupce: identifikátor a adresa v RAM paměti na [funkci/podrutinu]({{< relref "fce-podrutina2" >}}), která se má v případě přerušení zpracovat.

{{< figure align=center width=500 src="../interrupt2.png" title="Přerušení - krok 2" >}}

Jakmile je funkce/rutina zpracována tak tok instrukcí pokračuje tam, kde skončil před přerušením. 

{{< figure align=center width=500 src="../interrupt3.png" title="Přerušení - krok 3" >}}

Pohybování kurzorem po obrazovce generuje klidně stovky přerušení za vteřinu a každé toto přerušení znamená pohyb kurzoru myši z jednoho místa na obrazovce na jiné místo na obrazovce.

[^i]: *Anglicky interrupt*
[^s]: *Kurzor není nic jiného, než jen pár světélek (pixelů) na vašem monitoru.*
[^n]: *Jednoduchým příkladem je signál z klávesnice nebo myši.* 
[^t]: *IDT - Interrupt Descriptor Table*