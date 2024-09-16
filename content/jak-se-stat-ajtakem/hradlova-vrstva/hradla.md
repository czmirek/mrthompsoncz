---
draft: false
title: Hradla
weight: 501
---

*Hradlová vrstva* je jen jiný pohled na elektronické obvody. V elektronických obvodech identifikujeme **hradla** což jsou jednoduché logické funkce.

Každé hradlo má nějaké signály na vstupu a nějaké na výstupu. Hradla se zakreslují podle typu logické funkce, kterou představují.

Čipy jako je procesor nebo grafický čip obsahují miliardy rozhodovacích hradel. Díky tomuto obrovskému množství hradel vznikají další vrstvy a komplikovanější systémy. 

## Odbočka k bitům

O bitech mluvím velmi podrobně v kapitole o bitové vrstvě, která je v mém pojetí až nad hradlovou vrstvou. Správně bych měl v této kapitole ještě mluvit o signálech tj. *je signál* a *není signál*.
 
V tuto chvíli si stačí zapamatovat: bit je interpretace signálu který je buď 1 nebo 0.

Tzn.: 

- *je signál* = 1
- *není signál* = 0

## Základní hradla

**AND hradlo** - na výstupu je signál pouze pokud na všech vstupech je signál
{{< figure align=center width=500 src="../img/andhradlo.gif" title="AND hradlo" >}}

**OR hradlo** - na výstupu je signál pokud je aspoň na jednom vstupu signál
{{< figure align=center width=500 src="../img/orhradlo.gif" title="OR hradlo" >}}

**NOT hradlo** - na výstupu je signál opačný ke vstupu
{{< figure align=center width=500 src="../img/nothradlo.gif" title="NOT hradlo" >}}

**XOR hradlo** - na výstupu je signál pouze pokud počet signálů na vstupu je lichý
{{< figure align=center width=500 src="../img/xorhradlo.gif" title="XOR hradlo" >}}

**NAND hradlo**
{{< figure align=center width=500 src="../img/nandhradlo.gif" title="NAND hradlo" >}}

**NOR hradlo**
{{< figure align=center width=500 src="../img/norhradlo.gif" title="NOR hradlo" >}}

**XNOR hradlo**
{{< figure align=center width=500 src="../img/xnorhradlo.gif" title="XNOR hradlo" >}}

**Zajímavost**: S kombinací NAND hradel lze nasimulovat jakékoliv jiné hradlo
