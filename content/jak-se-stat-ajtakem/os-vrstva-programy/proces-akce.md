---
draft: false
title: Ukončení procesu
weight: 200900
---

Běžící proces lze v každém OS ukončit **dvěma hlavnímy způsoby** [^k]

- Signál běžného ukončení
- Zabití procesu

## Signál běžného ukončení

V OS Windows má většina běžných aplikací nějakou grafickou reprezentaci "okna" a ukončení aplikace je iniciované obyčejným kliknutím na křížek v pravém rohu okna. Pokud má program jen jedno okno pak to většinou znamená, že se ukončuje celý proces.

{{< figure align=center width=100 src="../winclose.png" title="Zavření programu" >}}

Podobně to funguje napříč všemi operačními systémy.

Co se reálně děje je, že OS vyšle danému procesu **signál pro ukončení**. Tento signál může aplikace zpracovat **jak je libo** --- toto závisí jednoduše na autorovi aplikace, jak se rozhodl toto implementovat.

Pokud například vytvoříte nový dokument ve Wordu, něco tam napíšete, neuložíte to a okno se pokusíte zavřít tak pak se vás přímo Word zeptá, jestli jste to náhodou nechtěli uložit.

⚠️ **Důležité je si zapamatovat**, že OS pouze zašlou signál a program sám se musí rozhodnout, jestli se chce na žádost uživatele zavřít nebo ne.

## Zabití procesu (process kill)

Každý proces lze "*zabít*". Nezapomeňte, že OS má plnou kontrolu nad svými procesy. Na uživatelskou žádost lze libovolný proces ukončit aniž bychom se toho procesu ptali na jeho názor nebo mu zasílali nějaký signál.

⚠️ **Avšak POZOR:** Zabití procesu znamená, že procesu **nedáte možnost dokončit svůj normální tok instrukcí**. Neustálé zabíjení procesů v běžné ajťácké praxi téměř vždy znamená problémy. 

[^k]: *Zjednodušeně řečeno. Těch signálů je v [Linuxu víc](https://www.gnu.org/software/libc/manual/html_node/Termination-Signals.html) ale to už jsou detaily které běžný ajťák znát nepotřebuje.*