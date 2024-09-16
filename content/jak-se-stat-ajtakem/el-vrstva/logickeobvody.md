---
draft: false
title: Logické el. obvody
weight: 307
---

Představte si jednoduchý obvod, ve kterém máte dva spínače za sebou.

{{< figure align=center width=400 src="../andobvod.png" title="AND obvod" >}}

Aby se žárovka rozvsítila, musí být sepnuté oba spínače. Jednoduché, že ano.

---

Nyní si představte jiný obvod, ve kterém máte dva spínače vedle sebe.

{{< figure align=center width=300 src="../orobvod.png" title="OR obvod" >}}

Aby se žárovka rozsvítila v tomto obvodu tak stačí, aby byl sepnutý jen jeden spínač. Z pohledu elektřiny už tady existuje uzavřený obvod a žárovka se rozsvítí. Stejně tak se žárovka rozsvítí i když budou zapnuté oba spínače.

Jinými slovy jsme si teď definovali **jednoduchou rozhodovací logiku**

- *vše* - musí být sepnuté všechny spínače
- *aspoň jeden* - musí být sepnutý aspoň jeden spínač

## Vzdálené sepnutí obvodu

Počítače obsahují obrovské množství obvodů. Výkonné čipy jako procesor nebo čipy na grafické kartě obsahují miliardy obvodů.

Tyto obvody se navzájem ovlivňují a díky tomu vznikají větší, logické struktury které pracují s podstatně složitější logikou než s tou uvedenou výše --- těmi se však budeme zabývat až v digitální vrstvě.

V elektronické vrstvě nám stačí vědět, jak se jednotlivé obvody ovlivňují.

### Relé

Relé je mechanický spínač, který je možno zapnout/vypnout z jiného obvodu.

{{< figure align=center width=500 src="../rele.png" title="Relé" >}}

Díky tomuto *"ovlivňování obvodů z jiných obvodů"* můžete postavit opravdu komplikované systémy. Tak komplikované a komplexní, jakým je například procesor.

**V běžných počítačích a ani procesorech se žádná relé nenachází.** Relé jsou však skvělá pro pochopení, jak se obvody v počítačích vzájemně ovlivňují. 

### Tranzistor

V počítačích se nepoužívají relé ale **tranzistory**.

Tranzistor je zařízení, které je oproti relé:

- mnohonásobně levnější a jednodušší na výrobu
- neobsahují žádné mechanické prvky které mají mnohonásobně větší poruchovost

Tranzistor obsahuje kombinaci různých polovodivých materiálů v závislosti na proudu v jiném obvodu. Tranzistorů je víc druhů (podle způsobu jakým jsou polovodivé materiály za sebou naskládané) ale přesný princip fungování není pro běžného ajťáka podstatný.

Zakreslení tranzistoru je v el. diagramu složitější, než u relé, není však podstatné jej znát. Pointou je, že v počítačích se tranzistor používá pro tentýž účel --- pro ovlivnění jednoho obvodu druhým.

Moderní procesory obsahují miliardy tranzistorů. Přestože mají tranzistory složitější zapojení, jsou extrémně levné na výrobu a proto díky nim došlo k počítačové revoluci, kdy dnes má počítač každý ať už ve formě telefonu, herní konzole, notebooku, tabletu nebo stolního počítače.