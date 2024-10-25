---
draft: false
title: Nedefinovaný obsah paměti
weight: 217000
---

OS procesům poskytuje libovolné množství paměti, stačí si o něj jenom říct - neboli **alokovat**. Jakmile proces paměť nepotřebuje, měl by tuto paměť "vrátit" - neboli **dealokovat**. 

<div class="note-blue">

**☝️ Otázka:** Co obsahuje paměť, kterou proces čerstvě alokoval? 

<ol type="A">
  <li>Jsou to všechno nuly? </li>
  <li>Nebo jedničky? </li>
  <li>Nebo je to složitější?</li>
</ol>

</div>

**Odpověď**: C. - je to složitější.

## Bity RAM paměti po zapnutí počítače

Jakmile **vypnete** počítač tak se bitový obsah v RAM paměti nenávratně ztratí.

Ale.

Jakmile **zapnete** počítač tak obsah RAM paměti je **nedefinovaný** což znamená:

- Mohou to být všechno 1
- Nebo 0
- Nebo úplně náhodně 0 a 1

V moderních RAM pamětích je to většinou ta třetí varianta - RAM paměť po zapnutí obsahuje "*náhodný bordel*". Toto není záměr ale vedlejší efekt toho, jak jsou RAM paměti vyrobené.

## Nedefinovaný obsah

Jakmile vám OS přidělí nějakou paměť tak ten její obsah je také **nedefinovaný** ale ještě z dalších důvodů.

- Může to být "náhodný obsah" RAM paměti po zapnutí počítače
- Mohou to být bity, které jste už dealokovali
- Nebo to mohou být bity, které dealokoval **jiný proces**

Paměti v tomto stavu se také říká, že je **neinicializovaná**.

**Inicializace** paměti je název pro operaci, kdy všechny bity ve své paměti přepíšete něčím konkrétním.
