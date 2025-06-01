---
draft: false
title: Funkce / podrutina
weight: 70330
description: Jak lze v instrukcích nadefinovat podrutiny díky JUMP instrukci
---

Díky **JUMP** instrukci je možné definovat **funkce** což jsou opakovaně použitelné bloky instrukcí. 

Na úrovni [strojového kódu]({{< relref "instrukce" >}}) se funkcím říká anglicky **subroutine** česky **podrutiny**.

Funkce je jednoduše nějaká část instrukcí, která má začátek a konec a kterou lze volat opakovaně. 

Po zavolání funkce se vrátíte zpět do původního toku instrukcí.

{{< figure align=center width=500 src="../podrutina.png" title="Funkce / podrutina" >}}

## Podrutina s JUMP instrukcí

Podívejte se na obrázek níže. Funkce je umístěná mezi adresami `[0x01]` až `[0x0F]`.

- Na začátku programu funkci volat nechceme, proto ji instrukcí `JUMP [0x10]` přeskočíme na adresu `[0x10]` (skok (1)).
- Provedou se instrukce na adresách `[0x10]` až `[0x12]`.
- Řekněme, že teď chceme zavolat podrutinu.
- Adresu `[0x00]` v JUMP instrukci na adrese podrutiny `[0x0F]` přepíšeme na hodnotu `0x15` instrukcí `MOV [0x0F], 0x15` [^m] 
- Další instrukcí `JUMP [0x01]` (skok (2)) vstoupíme do samotné funkce. Ta se začne provádět.
- Jakmile je celá funkce provedena, vrátíme se instrukcí `JUMP [0x15]` (skok (3)) zpět tam, kde jsme skončili tj. na adresu `[0x15]`.

{{< figure align=center width=500 src="../subroutine2.png" title="Funkce / podrutina" >}}

[^m]: *Toto je pouze ilustrace, reálné použití instrukce `MOV` vypadá trochu jinak a může se lišit mezi instrukčními sadami.*