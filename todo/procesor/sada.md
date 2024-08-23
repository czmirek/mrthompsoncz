---
draft: true
title: Instrukční sada
weight: 252
---

## Formát instrukce a instrukční sada   

Velikost instrukce odpovídá počtu vstupních signálů (0 nebo 1) — toto je fyzický počet drátů, které uvnitř procesoru reprezentují konkrétní instrukci.

Moderní procesory mají 64 vstupních signálů. Konkrétní instrukce může vypadat třeba takto:

0000000000000000000000000000000000000000000000000000000000000000
(všude 0 znamená, že v žádném „instrukčním drátu“ v danou chvíli nejde proud).

Instrukce se skládá ze dvou částí:

- **typ instrukce** – toto říká, co procesor má udělat
- **data** – většina instrukcí vyžaduje ještě nějaké informace navíc. Může jít například o adresu v paměti nebo konkrétní hodnotu která se má někam uložit, například pro dokončení nějaké matematické operace.

Každý procesor je postavený pro specifickou instrukční sadu – to je prostě jenom dohodnutý kód který pojmenovává všechny instrukce, které procesor umí. Nejmodernější instrukční sady jsou:


- **x86** – starší počítače a procesory.
  - Šířka instrukce: 32
- **x86-64** (nebo jen **x64**) – rozšíření x86, prakticky ve všech počítačích a notebocích všude na světě.
  - Šířka instrukce: 64
- **ARM** – mobilní telefony a tablety
  - Šířka instrukce: 32 a 64 (ARM64)

**Zajímavost:** oficiální dokumentace k x86-64 má [2198 stránek](https://www.intel.com/content/dam/www/public/us/en/documents/manuals/64-ia-32-architectures-software-developer-instruction-set-reference-manual-325383.pdf) a k ARM64 má [8538 stránek](https://www.intel.com/content/dam/www/public/us/en/documents/manuals/64-ia-32-architectures-software-developer-instruction-set-reference-manual-325383.pdf)

Moderní procesory znají tisíce různých instrukcí a průměrný ajťák většinou žádnou instrukci nezná. Kdo si nějaké instrukce pamatuje tak většinou kvůli nějakému povinnému předmětu na vejšce.

Přímo na instrukcích dnes už jen velmi vzácně programují ajťáci, kteří potřebují vymáčknout z počítače co nejvyšší výkon – například vyrábí počítačové hry nebo jiný software, kde je kritický maximální výkon.

**Některé instrukční sady lze zaměnit, některé ne.**

- x86 program nebude běžet na ARM a naopak
- x86 program bude běžet na x86_64 ale ne naopak

## Teplota a spotřeba energie u procesoru

Různé instrukce jsou různě náročné. Pokud procesor provádí spoustu intenzivních matematických výpočtů, zaměstnává tím obvody které produkují spoustu tepla a spotřebovávají více energie. Proto procesory vyžadují nějakou formu chlazení.

## Rychlost procesoru

Jak rychle putuje elektřina v obvodech procesoru? Rychlostí světla (cca 299792 km/s). Technologie procesorů už dospěla do stavu, kdy rychlost světla je limitující faktor: je čím dál těžší postavit elektrický procesor, který by byl nějak podstatně rychlejší.

Většina moderních procesorů pro domácí použití by shořela kdyby rychlost procesoru nebyla nijak řízená. Proto jsou procesory řízené frekvencí se kterou instrukce dostávají (např. 5 Ghz = 5 miliard instrukcí za vteřinu). Výrobci procesorů balancují hodnoty frekvencí mezi teplotní stabilitou a výkonem.

<div class="note1">

**Zajímavost:** V moderních počítačích už nehrozí, že by něco shořelo. Moderní PC obsahují bezpečnostní čidla a jakmile teplota procesoru přesáhne nějakou hranici, frekvence procesoru se automaticky drasticky sníží třeba jen na 5-10% výkonu. Počítač začne být extrémně pomalý ale nezníčí se.

</div>

---

<div class="note1">

**Overclocking** je název pro zvýšení této frekvence nad doporučovaný údaj od výrobce procesoru (potom je nutné kvalitní chlazení aby se procesor nezníčil), toto je oblíbená praxe různých hráčů a kutilů, kteří chtějí z výkonu svého počítače vymáčknout maximum.

</div>

## Shrnutí

- Instrukce procesoru se dělí na typ instrukce a data.
- Nejpoužívanější instrukční sady dnešní doby jsou x86, x86-64 a ARM.
  - x86 program lze rozeběhnout na x86_64 ale ne naopak
  - ARM program lze rozeběhnout pouze na ARM, ne na x86 ani na x86-64
- Procesory běží na stanovené frekvenci. Výrobci procesorů balancují mezi rychlostí procesoru a jeho fyzickou stabilitou. Výkonné procesory vyžadují aktivní chlazení – nějakou žebrovanou, teplovodivou strukturu s větráčky, které odvádí horký vzduch pryč.
- Overclocking je zvýšení frekvence nad limity doporučované výrobcem.
