---
draft: false
title: CRLF
weight: 7120
---

Podívejte se ještě jednou na tabulku ASCII, konkrétně na kódy pod číslem 13 a 10.

{{< figure align=center width=200 src="../crlf.png" title="CR LF v ASCII" >}}

Tyto dva signály v textu za sebou reprezentují **nový řádek** formou dvou **historických instrukcí pro tiskárnu**:

- `CR = carriage return` = mechanická tisková hlava se posune na začátek stránky
- `LF = line feed` = papír v tiskárně se posune o jeden řádek výše.

Tisk v moderních tiskárnách probíhá skrz úplně jiné kódy a protokoly. Mechaniky a elektroniku v moderních tiskárnách není možné manipulovat napřímo skrz znakovou sadu, jako to šlo v minulosti. CRLF však zůstalo.


<div class="note-blue">

⚠️⚠️⚠️ **Extra důležité k zapamatování**

V IT světě bohužel existují paralelně **dvě konvence** pro reprezentování **nového řádku textu**.

- **CRLF** nebo také `\r\n` = kód používaný OS Windows a většinou softwaru psaného pro MS technologie.
- **LF**  nebo také `\n` = kód používaný ostatními OS (Unix, Linuxy, MacOS...) a většina softwaru v těchto OS.

</div>

<div class="note-blue">

**Pozor!**

- OS není zárukou, že software, se kterým pracujete, uloží nové řádky jako CRLF nebo jen LF.
- Bohužel narazíte i na mix CRLF a LF.
- Dobrý software si dokáže s mixem CRLF/LF poradit (např. internetový prohlížeč, populární textový editor atd.).
- Existuje spousta špatně napsaného softwaru, který si s tím poradit neumí.
- Někteří lidé z IT jsou schopni se kvůli CRLF/LF i hádat.

</div>