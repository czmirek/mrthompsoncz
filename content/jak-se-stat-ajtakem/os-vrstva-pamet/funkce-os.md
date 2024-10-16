---
draft: true
title: OS API nad virtuální pamětí
weight: 210700
---

<!-- 
Operační systémy skrz funkce OS API / syscalls umožňují programům:

- **vyžádat si další virtuální paměť**
- **vrátit již nepotřebnou virtuální paměti**

## Vyžádání virtuální paměti

- Pro vyžádání paměti proces zavolá funkci OS API (nebo syscall) pro to určenou a při zavolání této funkce musí uvést **požadovaný počet bajtů**.
- Na obrázku níže je požadavek na 4 bajty.
- OS API ve virtuální paměti najde **souvislý blok paměti** [^s] který procesu přiřadí v user space.
- A následně na požadavek procesu odpoví **adresou na první bajt virtuální paměti**.

{{< figure align=center width=700 src="../prideleni.png" title="Vyžádání virtuální paměti" >}}

## Vrácení virtuální paměti

Jakmile se proces rozhodne, že nějaký kus paměti již dále nepotřebuje tak jej může uvolnit zavoláním další OS API funkce.

V tomto případě proces zavolá funkci, které předá **adresu prvního 


[^s]: *Souvislý = adresy jednotlivých bajtů jdou za sebou.*
-- >