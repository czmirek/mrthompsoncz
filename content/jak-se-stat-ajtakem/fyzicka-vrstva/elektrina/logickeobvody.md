---
draft: false
title: Logické el. obvody
weight: 227
---

Představte si jednoduchý obvod, ve kterém máte dva spínače za sebou.

..obr AND obvodu..

Aby se žárovka rozvsítila, musí být sepnuté oba spínače. Jednoduché, že ano.

Nyní si představte jiný obvod, ve kterém máte dva spínače vedle sebe.

..obr OR obvodu..

Aby se žárovka rozsvítila v tomto obvodu tak stačí, aby byl sepnutý jen jeden spínač. Z pohledu elektřiny už tady existuje uzavřený obvod a žárovka se rozsvítí. Stejně tak se žárovka rozsvítí i když budou zapnuté oba spínače.

Jinými slovy jsme si teď definovali **jednoduchou rozhodovací logiku**

- *vše* - musí být sepnuté všechny spínače
- *aspoň jeden* - musí být sepnutý aspoň jeden spínač

## Vzdálené sepnutí obvodu

Počítače obsahují obrovské množství obvodů. Procesor obsahuje miliardy obvodů.

Tyto obvody se navzájem ovlivňují a díky tomu vznikají větší, logické struktury které pracují s podstatně složitější logikou než s tou uvedenou výše --- těmi se však budeme zabývat až v digitální vrstvě.

V elektronické vrstvě nám stačí vědět, jak se jednotlivé obvody ovlivňují.

### Relé

Relé je jednoduše mechanický spínač, který je možno sepnout z jiného obvodu.

...obr obvodu se spínačem...

V běžných počítačích se žádná relé nenachází, je to však jednodušší pro ilustraci, jak jeden obvod může ovlivnit druhý.

### Tranzistor

Tranzistor je zařízení složené z různých polovodivých materiálů. Tranzistorů je víc druhů (podle způsobu jakým jsou polovodivé materiály za sebou naskládané) ale přesný princip fungování není pro běžného ajťáka podstatný.

Zakreslení tranzistoru je v el. diagramu trochu složitější, pointou však je, že v počítačích se tranzistor používá pro tentýž účel --- pro ovlivnění jednoho obvodu druhým.

..obr obvodu s tranzistorem..

Moderní procesory obsahují miliardy tranzistorů. Přestože mají tranzistory složitější zapojení, jsou extrémně levné na výrobu a proto díky nim došlo k počítačové revoluci, kdy dnes má počítač každý ať už ve formě telefonu, herní konzole, notebooku, tabletu nebo stolního počítače.