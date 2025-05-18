---
draft: false
title: Logické el. obvody
weight: 307
description: Jak lze v elektrických obvodech vytvářet logické, "rozhodovací" obvody, co je relé a k čemu je v počítačích tranzistor
---

Představte si jednoduchý obvod se dvěma spínači za sebou.

{{< figure align=center width=400 src="../andobvod.png" title="AND obvod" >}}

Aby se žárovka rozvsítila, musí být sepnuté oba spínače. Jednoduché, že.

---

Nyní si představte další obvod, ve kterém máte dva spínače vedle sebe.

{{< figure align=center width=300 src="../orobvod.png" title="OR obvod" >}}

Aby se žárovka rozsvítila v tomto obvodu tak stačí, aby byl sepnutý jen jeden spínač. Stejně tak se žárovka rozsvítí i když budou zapnuté oba spínače.

Jinými slovy jsme si teď definovali **jednoduchou rozhodovací logiku**

- **vše** - musí být sepnuté všechny spínače
- **aspoň jeden** - musí být sepnutý aspoň jeden spínač

## Vzdálené sepnutí obvodu

Výkonné čipy jako procesor obsahují miliardy obvodů.

Obvody v procesorech **se navzájem ovlivňují** a díky tomu vznikají **větší, logické struktury** které pracují s podstatně složitější logikou než jen "vše/aspoň jeden".

Pro běžného ajťáka není podstatné vědět, jak se tyto obvody staví ale je zásadní pochopit princip vzdáleného sepnutí.

### Relé

Relé je mechanický spínač, který je možno zapnout/vypnout z jiného obvodu.

{{< figure align=center width=500 src="../rele.png" title="Relé" >}}

**V běžných počítačích a ani procesorech se žádná relé nenachází.** Je zde uvedené pouze pro ilustraci, co je myšlené principem vzdáleného sepnutí.

### Tranzistor

V počítačích se nepoužívají relé ale **tranzistory**.

Tranzistor je zařízení, které je oproti relé:

- mnohonásobně levnější a jednodušší na výrobu než relé
- neobsahuje žádné mechanické prvky které mají mnohonásobně větší poruchovost

Tranzistor obsahuje kombinaci různých polovodivých materiálů v závislosti na proudu v jiném obvodu. Tranzistorů je víc druhů (podle způsobu jakým jsou polovodivé materiály za sebou naskládané) ale přesný princip fungování není pro běžného ajťáka podstatný.

<div class="note-blue">

⚠️ V počítačích se tranzistor používá pro ovlivnění jednoho obvodu jiným obvodem pro vytvoření větších a složitějších rozhodovacích celků.

</div>

Moderní procesory obsahují miliardy tranzistorů. Tranzistory mají složitější zapojení, než relé, ale jsou extrémně levné na výrobu a proto díky nim došlo k počítačové revoluci, kdy dnes má počítač každý ať už ve formě telefonu, herní konzole, notebooku, tabletu nebo stolního počítače.