---
draft: false
title: 'Stack segment: call stack'
weight: 212000
---

**Stack segment** nebo jen **stack** je paměť dedikovaná [podrutinám]({{< relref "../procesor/fce-podrutina" >}}).

Nejdřív bych rád připomněl kapitolu o [řetězení podrutin]({{< relref "../procesor/retezeni-podrutin" >}}), konkrétně následující obrázek.

{{< figure align=center src="../retezeni.gif" title="Řetězení podrutin" >}}

## Call stack

Pro každé **vlákno** programu operační systém přiřadí **call stack** [^t] což je jednoduše kus virtuální paměti, který se může nafukovat a zase smršťovat.

**Call stack** je něco jako nádoba, do které lze házet kostičky na sebe. Vyndat ale můžete jenom tu nejhornější kostičku. Tomu se také říká **LIFO** struktura [^l] . Jednotlivým kostičkám se říká **stack frame** což je jen kus virtuální paměti dedikovaný pro dané **volání podrutiny**. 

V rámci **[volací konvence]({{< relref "calling-convention" >}})** vzniká pro každou volanou podrutinu **stack frame**.

{{< figure align=center width=200 src="../sf.gif" title="Call stack" >}}

Celá věc začne dávat mnohem větší smysl s obrázkem pro řetězení podrutin.

{{< figure align=center src="../retezeni.gif" title="Řetězení podrutin" >}}

<div class="note-blue">

⚠️ **Důležité k zapamatování**

- Jakmile je podrutina dokončena, její stack frame se odstraní.
- Jakmile skončí celé vlákno, odstraní se i celý jeho call stack.

</div>

[^t]: *Nebo "thread stack" ale myslí se tím jedno a totéž. Do češtiny se nepřekládá.*
[^l]: *Last In First Out - poslední uvnitř, první ven*