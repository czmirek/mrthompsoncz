---
draft: false
title: Komponenty
weight: 120
---

Na počítače se také můžeme dívat podrobnějším pohledem, kdy se ptáme na jednotlivé komponenty, které se v počítačích nachází.

Tyto komponenty se rozdělují do dvou skupin:
- **základní komponenty** tedy ty, bez kterých moderní a běžný počítač nemůže být počítačem.
- **vstupy a výstupy**

## Základní komponenty

- **Procesor** = nejdůležitější část, která dělá počítače počítačem. Procesoru se budu v tomto návodu věnovat nejvíce.
- **RAM paměť** = "živá" a "rychlá" paměť počítače, kde se nachází data, se kterými procesor právě pracuje. Obsah paměti je ztracen, jakmile je počítač vypnutý.
- **Základní deska** (motherboard) = integrovaný obvod, který komponenty propojuje. 

## Vstupy a výstupy

Veškerá ostatní zařízení lze oddělit na vstupy a výstupy.

- **Vstupy** = zařízení, která posílají data do počítače
  - Příklad: klávesnice, myš
- **Výstupy** = zařízení, která přijímají data od počítače
  - Příklad: tiskárna
- **Kombinovaná** = zařízení, která posílají data do počítače a zároveň přijímají data od počítače.
  - Příklad: disky (čtení a zápis), síťová karta, multifunkční tiskárny/skenery, atd.

## Von Neumannova architektura

Komponenty moderních počítačů jsou dodnes stavěny podle Von Neumannovy architektury.

- Procesor je napřímo propojený s RAM pamětí do které čte a zapisuje
- Do procesoru proudí data přes vstupní signály - od vstupních zařízení
- A naopak: z procesoru proudí data přes výstupní signály - do výstupních zařízení

{{< figure align=center width=400 src="/jak-se-stat-ajtakem/uvod-do-it/vonneumann.png" title="Von Neumannova architektura" >}}

Základní deska není zakreslena. Přestože se moderní počítače bez základní desky neobejdou, není to až tak zajímavá komponenta a později v tomto návodu pochopíte proč.