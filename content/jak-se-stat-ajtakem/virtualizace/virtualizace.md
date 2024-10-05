---
draft: false
title: Virtualizace
weight: 70800
---

Virtualizace je **schopnost procesoru simulovat jiné procesory** a potažmo **celé počítače**. Na jednom procesoru jste díky virtualizaci schopni simulovat další počítače. 

{{< figure align=center width=400 src="../virtualizace.png" title="Virtualizace" >}}

Běžný ajťák by však měl chápat rozdíl mezi **softwarovou virtualizací** a **hardwarovou virtualizací** už na úrovni procesoru.

## Softwarová virtualizace

Softwarová virtualizace je logická vlastnost každého [univerzálního turingova stroje]({{< relref "turinguv-stroj" >}}). 

Univerzální turingův stroj dokáže simulovat jakýkoliv jiný turingův stroj i jakýkoliv jiný univerzální turingův stroj --- tzn. procesor dokáže simulovat jiný procesor. 

Jak by to vypadalo v praxi? Jednoduše musíte mít k dispozici **program** tedy **bitové instrukce**, kterými jiný procesor **simulujete**. Váš program je simulací procesoru, RAM paměti a klidně i jakýchkoliv jiných komponent. Tento váš nasimulovaný procesor má svoji vlastní instrukční sadu a svoji vlastní logiku chování.

### Nevýhody softwarové virtualizace

Pokud chcete na reálném počítači simulovat jiný moderní počítač tak musíte simulovat úplně vše, co k tomu patří: chipset základní desky, procesor, RAM paměť, sběrnice, nějaké komponenty a podobně. 

Taková simulace je i pro moderní procesory dost náročná. Sice teď máte dva počítače ale jeden je příšerně pomalý a druhý je na tom ještě hůř. 

## Hardwarová virtualizace

Virtualizace je v IT průmyslu tak často využívaný mechanismus, že se pro tento účel začaly přizpůsobovat i moderní procesory a instrukční sady.

V rámci instrukce vstupující do procesoru jsou některé bity určené pro identifikaci **virtuálního procesoru**.

**Příklad:** 

- V normálním provozu vypadá instrukce pro procesor následovně: <span style="color:red">1101</span><span style="color:orange">100110101011</span><span style="color:green">00000000</span> --- červená je kód instrukce, oranžově jsou data, zeleně jsou nevyužité bity instrukce
- Ve virtualizovaném tatáž instrukce vypadá následovně procesor následovně: <span style="color:red">1101</span><span style="color:orange">100110101011</span><span style="color:green">000000</span><span style="color:blue">01</span> --- modře je identifikátor virtuálního stroje. 00 je normální provoz, 01 až 11 jsou 3 virtuální stroje.

Tímto způsobem je výkonnost virtuálních počítačů podstatně vyšší --- prostě se jenom dělí o instrukce s reálným počítačem. Zatímco u softwarové virtualizace musíte napsat aplikaci, která simuluje procesor kompletně se vším všudy, u hardwarové virtualizace jsou instrukce virtuálního procesoru obsluhovány reálným procesorem.

Toto je možné pouze tehdy, pokud procesor HW virtualizaci podporuje, což v dnešní době umí téměř všechny.