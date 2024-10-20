---
draft: false
title: 'Řídící instrukce: podrutiny'
weight: 70330
---

Díky **JUMP** instrukci je možné definovat **funkce**. Na úrovni strojového kódu se funkcím říká anglicky **subroutine** česky **podrutiny**.

Funkce je jednoduše nějaká část instrukcí, která má začátek a konec a kterou lze volat opakovaně. 

Po zavolání funkce se vrátíte zpět do původního toku instrukcí.

{{< figure align=center width=500 src="../podrutina.png" title="Funkce / podrutina" >}}

## Příklad s JUMP instrukcí

Podívejte se na obrázek níže. Funkce je umístěná mezi adresami 2 až 10.

{{< figure align=center width=500 src="../subroutine2.png" title="Funkce / podrutina" >}}

1. Na začátku programu funkci volat nechceme, proto ji instrukcí `JUMP 11` přeskočíme. Z adresy 1 se dostaneme na adresu 11.
2. Provedou se instrukce na adresách 11, 12, 13 a následně číslo 0000 na adrese 10 přepíšeme na číslo 16 instrukcí `MOV 10,16` [^m] 
3. Další instrukcí `JUMP 2` vstoupíme do samotné funkce. Ta se začne provádět.
4. Jakmile je celá funkce provedena, vrátíme se instrukcí `JUMP 16` zpět tam, kde jsme skončili tj. na adresu 16.

[^m]: *Toto je pouze ilustrace, reálné použití instrukce `MOV` vypadá trochu jinak a může se lišit mezi instrukčními sadami.*