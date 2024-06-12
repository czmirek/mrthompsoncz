---
draft: false
title: Multithreading
weight: 570
---

V minulém díle jsem pojmenoval pojmy jako proces, entry point, vlákno, hlavní vlákno a stavy vláken.

Operační systém má na starost evidenci, vytváření a přidělování vláken. Jak se ale operační systém rozhoduje, které vlákno má zrovna běžet?

## HALT instrukce

Už víte, že procesor je zařízení, do kterého se neustále sypou instrukce. Jakmile zapnete počítač a nic na něm neděláte tak to operační systém kompenzuje HALT instrukcí, která prostě jen pozastaví procesor na krátký časový úsek, třeba 0,0001 vteřiny.

## Context switching

Jakmile začnou v počítači vznikat další vlákna, operační systém jednoduše sníží počet HALT instrukcí a uvolní výpočetní kapacitu procesoru novému vláknu.

Vláken může běžet najednou libovolné množství – jsme omezeni pouze pamětí a výkonem procesoru.

Jenže bacha – vzpomeňte si, jak funguje procesor: zpracovává instrukce za sebou. Procesor (jednoduchý, jednojádrový procesor) neumí zpracovávat několik instrukcí současně. Jasně, umí zpracovat 5 miliard instrukcí za vteřinu ale neumí zpracovat 2 instrukce najednou, ve stejný čas. Instrukce zpracovává v sérii (za sebou) nikoliv paralelně (vedle sebe).

Jak to tedy operační systémy dělají, že umožňují paralelní běh několika vláken najednou?

Neumožňují.

OS neustále přepíná mezi tím, které vlákno má zrovna přidělený čas procesoru. Tomuto přepínání se říká context switching a schopnosti takto spouštět jednotlivá vlákna se říká multithreading.

![Multithreading](/jak-se-stat-ajtakem/os-vrstva/Multithreaded_process.svg)

To je celé.

Plyne z toho jeden závěr: se zvyšujícím se počtem běžících vláken se zpomaluje rychlost každého běžícího vlákna, jinými slovy, zpomaluje se na oko práce s celým počítačem.

Moderní procesory jsou však tak brutálně rychlé, že z pohledu lidského vnímání na nich mohou běžet stovky vláken „najednou“. Ve zlomku vteřiny procesor přidělí dostatečný čas každému vláknu a z pohledu uživatele všechny vlákna běží paralelně.

Obrázek níže ilustruje celkovou kapacitu procesoru. Pokud má procesor 5 GHz, pak zvládne 5 miliard instrukcí za vteřinu. Operační systém a veškerý software, který pod OS běží, si díky context switchingu bere kousek této kapacity pro sebe.

![Multithreading 2](/jak-se-stat-ajtakem/os-vrstva/multithreading.drawio.png)

## OS Scheduler

OS Scheduler je název pro tu část operačního systému, která se stará o správu běžících procesů, vláken a o context switching.

V IT je však scheduler obecnější název pro jakýkoliv mechanismus, který má na starosti nějaké plánování.

## Vícejádrové procesory

Moderní procesory jsou ve skutečnosti „multičipy“, které obsahují několik „podprocesorů“ kterým se říká „jádra“. Například „procesor s 8 jádry“ ve skutečnosti lze označit za „8 procesorů“, které běží paralelně, každý s frekvencí 5 miliard instrukcí za vteřinu.

Vícejádrových procesory umožňují, aby instrukce skutečně probíhaly paralelně. V jakém jádru ale běží jaké konkrétní vlákno si automaticky určuje operační systém. Windowsy a Linuxy umožňují přiřazení vlákna na konkrétní jádro pomocí tzv. afinity ale za celou svoji praxi jsem nikdy neměl situaci, že bych potřeboval afinitu vlákna nastavovat.

Multithreading je podporován v každém jádře. V každém jádře stále může běžet více vláken najednou ale díky většímu počtu jader lze provozovat větší počet vláken bez znatelné ztráty výkonu v porovnání s jednojádrovým procesorem.

Nelze ale automaticky říct, že procesor s více jádry je výkonnější, než jednojádrový procesor. Záleží na použití.

Aplikace, která spouští značné množství vláken, jako např. počítačová hra, bude těžit z vyššího počtu jader víc, než z jednojádrového procesoru. Aplikace, ve které běží jen jedno vlákno, bude běžet stejně rychle na jednojádrovém i vícejádrovém procesoru.

## Shrnutí


- HALT je instrukce, kterou operační systém v procesoru spouští, pokud zrovna nemá co dělat. Tato instrukce na velmi krátký časový úsek procesor pozastaví.
- Procesor, nebo jádro procesoru, zpracovává instrukce vlákna v sérii = za sebou = nejdřív zpracuje jednu instrukci a pak tu, která za ní následuje.
- Multithreading je schopnost spouštět několik vláken na jednou – ve skutečnosti operační systém neustále přepíná přidělený čas procesoru běžícím vláknům. Tomuto přepínání se říká context switch.
- Moderní procesory jsou ve skutečnosti „multiprocesory“ – je to několik procesorů najednou. Těmto podprocesorům se říká „jádra“.
- Operační systém určuje, jaké vlákno běží v jakém jádře.