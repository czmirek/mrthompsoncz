---
draft: true
title: Procesor
weight: 250
layout: single2
---

Moderní počítače jsou orientované na software a od běžného uživatele se neočekává, že se bude snažit cokoliv dělat s pájkou. Stolní počítače/notebooky se skládají z komponent, které lze k sobě jednoduše spojit nebo přišroubovat. V moderních telefonech tato možnost ani neexistuje, jsou to hotová zařízení kde se neočekává, že se v tom obyčejný uživatel bude hrabat.

Historicky byly počítače obří „procesory“ které obstarávaly všechny instrukce, které jim byly zadané. Až později se začaly některé funkce z procesoru přesouvat do specializovaných zařízení.

Prakticky se dá říct, že počítač je procesor. Vše ostatní lze roztřídit na:

- základní desku
- vstupy a výstupy
- uložiště a paměť

![Základní deska](/jak-se-stat-ajtakem/fyzicka-vrstva/VonNeumann.jpg)

## Základní deska

Základní deska (neboli motherboard) je integrovaný obvod obsahující spoustu vlastních čipů a dalších obvodů. Hlavním účelem základní desky je procesor propojit se vstupy a výstupy a efektivně přenášet data mezi zařízeními pracujícími na jiných rychlostech. Přestože základní deska je celkem komplexní zařízení samo o sobě tak pro nás ajťáky je důležitá jen proto, protože na ni potřebujeme umístit procesor.


## Vstupy

Jakékoliv zařízení, ze kterého data mohou proudit směrem do procesoru.
Příklady: myš, klávesnice, dotyková obrazovka, scanner, webkamera…

## Výstupy

Jakékoliv zařízení, do kterého data mohou proudit směrem z procesoru.
Příklady: grafická karta a obrazovka, tiskárna, zvuková karta.

## Kombinovaný vstup a výstup

Spousta zařízení umožňuje jak vstup tak i výstup.
Příklady: síťová karta, WiFi, bluetooth, multifunkční tiskárna…

## Uložiště a paměť

Jakékoliv uložiště spadá pod kombinovaný vstup a výstup. Procesor může z uložiště číst (takže jde o vstup) ale může do uložiště i zapisovat (takže jde i o výstup). Za uložiště se považuje jakékoliv zařízení, kde jsou data „uložena“ i po odpojení od elektřiny (tzn. vypnutí počítače). Mezi tato uložiště patří HDD, SSD, Flash Disky, SD karty a podobně.

Procesor teoreticky může s každým uložištěm pracovat napřímo, prakticky se to však neděje, protože uložiště jsou pro procesor příliš pomalá.

Procesor místo toho instruuje základní desku, aby data připravila do paměti která je extra rychlá (avšak také mnohem dražší a s mnohem menší kapacitou). Jakmile počítač vypnete, veškeré informace z paměti se ztratí (režim spánku přesune obsah paměti do uložiště). Této paměti se říká RAM (co přesně to znamená není teď důležité), u stolních PC/notebooků jsou to takové destičky které lze do základní desky zapojit a tím si paměť rozšířit. U telefonu je zpravidla RAM paměť zabudovaná napevno a nelze ji rozšířit.

<div class="note1">

**Na vzdálenosti záleží:** Moderní procesory jsou tak extrémně rychlé, že již naráží na limity fyzikálních možností. Jedním z těchto limitů je rychlost světla, kterou elektřina v procesoru putuje. Protože rychlost světla nemůže být rychlejší tak i fyzická vzdálenost mezi jednotlivými komponenty je důležitý faktor.

</div>

<div class="note1">

**Zajímavost:** V dnešní době lze sestavit počítač, kde RAM běží na rychlejší frekvenci než samotný procesor. Základní deska pak automaticky RAM zpomalí na stejnou frekvenci procesoru, jinak by s ní procesor nemohl pracovat.

</div>

## Von Neumannova architektura

Procesor, vstupy, výstupy a paměť a uložiště propojené dohromady je koncept z roku 1945 vymyšlený jistým Von Neumannem, který víceméně platí dodnes (základní deska jeho modelu obsažena nebyla, stejně tak procesorová cache a podobně).

## Shrnutí

- Hlavní komponentou počítače je procesor.
- Vše ostatní se v počítači dělí na vstupy a výstupy.
- Procesor pro práci s daty potřebuje rychlou paměť a nikdy nepracuje s persistentním uložištěm napřímo.
