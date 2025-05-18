---
draft: false
title: Hradlová vrstva
weight: 501
---

*Hradlová vrstva* je vrstva ležící na signální vrstvě. 

**Hradlo** je logická funkce se signály na vstupu a na výstupu. Hradla se zakreslují podle typu logické funkce, kterou představují.

Čipy jako je procesor nebo grafický čip obsahují miliardy rozhodovacích hradel. Díky tomuto obrovskému množství hradel vznikají další vrstvy a komplikovanější systémy.

Hradla a hradlová vrstva jsou důležitá pro pochopení dalších vrstev. Běžný ajťák se hradly či hradlovou vrstvou napřímo nezabývá, to je stále spíš doména elektrotechniky.

## Základní hradla

**AND hradlo** - logické "a". Signál je na výstupu pouze tehdy, pokud první **a** druhý vstup obsahuje signál.

{{< figure align=center width=500 src="../img/andhradlo.gif" title="AND hradlo" >}}

**OR hradlo** - logické "nebo". Signál je na výstupu, pokud první **nebo** druhý výstup obsahuje signál.
{{< figure align=center width=500 src="../img/orhradlo.gif" title="OR hradlo" >}}

**NOT hradlo** - na výstupu je signál opačný ke vstupu
{{< figure align=center width=500 src="../img/nothradlo.gif" title="NOT hradlo" >}}

**XOR hradlo** - na výstupu je signál pouze pokud počet signálů na vstupu je lichý
{{< figure align=center width=500 src="../img/xorhradlo.gif" title="XOR hradlo" >}}

**NAND hradlo** - kombinace NOT a AND hradla
{{< figure align=center width=500 src="../img/nandhradlo.gif" title="NAND hradlo" >}}

**NOR hradlo** - kombinace NOT a OR hradla
{{< figure align=center width=500 src="../img/norhradlo.gif" title="NOR hradlo" >}}

**XNOR hradlo** - kombinace NOT a XOR hradla.
{{< figure align=center width=500 src="../img/xnorhradlo.gif" title="XNOR hradlo" >}}

**Zajímavost**: S kombinací NAND hradel lze nasimulovat jakékoliv jiné hradlo
