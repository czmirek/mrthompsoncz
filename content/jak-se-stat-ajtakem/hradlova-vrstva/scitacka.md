---
draft: false
title: Binární sčítačka
weight: 503
---

Binární sčítačka je sestavení hradel takovým způsobem, že určitá skupina vstupů reprezentuje jedno číslo, druhá skupina vstupů reprezentuje druhé číslo a na výstupu je výsledek po sečtení.

Je mnoho způsobů, jak lze sčítačku z hradel postavit. Na následujícím obrázku je nejjednodušší sčítačka, která sečte 2 bity.

*(Pozn: O dvojkové/desítkové soustavě se dočtete později v kapitole o bitových interpretacích.)* 

{{< figure align=center width=500 src="../img/scitacka_2bit.gif" title="2 bitová sčítačka" >}}

Jakmile začnete chtít sčítat víc jak 2 bity, potřebujete podstatně víc hradel. Fakt není nutné si tyto obrázky pamatovat. Je nutné chápat pouze ten princip, jakým způsobem vlastně dokážeme díky signálům sčítat dvě čísla.

{{< figure align=center width=500 src="../img/4-bit-full-adder.png" title="4 bitová sčítačka" >}}

## Násobení, odčítání, dělení

Hradla lze postavit i tak, aby uměla násobit, odčítat, dělit ale upřímně nedává mi moc smysl sem dávat obrázky, jak vypadají hradlová schémata těchto operací, většina profesionálních ajťáků podle mně z hlavy nedá ani tu základní 2-bitovou sčítačku.

Není vůbec nutné si toto pamatovat, pokud vás vyloženě neláká hrát si se signální vrstvou. Pokud jo, doporučuji [CircuitVerse](https://circuitverse.org/).