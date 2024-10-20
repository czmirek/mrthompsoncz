---
draft: false
title: 'Stack segment: call stack'
weight: 212000
---

**Stack segment** je už trochu složitější struktura.

## Řetězení podrutin

Aplikace zavolá podrutinu. Tato podrutina zavolá další podrutinu. A tak dále. Ve výsledku dochází k řetězení podrutin. 

V moderních procesorech se u některých aplikací podrutiny mohou řetězit klidně až na tisíce podrutin. Níže je zpomalená ilustrace řetězení podrutin v nějakém jednoduchém programu.

{{< figure align=center src="../retezeni.gif" title="Řetězení podrutin" >}}

## Call stack

Pro každé **vlákno** programu operační systém přiřadí **call stack** [^t] což je jednoduše kus virtuální paměti. 

**Call stack** je něco jako nádoba, do které lze házet kostičky na sebe. Vyndat ale můžete jenom tu nejhornější kostičku. Tomu se také říká **LIFO** struktura [^l] . Těmto kostičkám se říká **stack frame** což je jen kus virtuální paměti dedikovaný pro dané **volání podrutiny**.

V rámci **[volací konvence]({{< relref "calling-convention" >}})** vzniká pro každou volanou podrutinu **stack frame**.

{{< figure align=center width=200 src="../sf.gif" title="Call stack" >}}

Dále je důležité si zapamatovat, že:

- Jakmile je podrutina dokončena, její stack frame se odstraní.
- Jakmile skončí celé vlákno, odstraní se i celý jeho call stack.

[^t]: *Nebo "thread stack" ale myslí se tím jedno a totéž. Do češtiny se nepřekládá.*
[^l]: *Last In First Out - poslední uvnitř, první ven*