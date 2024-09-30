---
draft: true
title: Proces a vlákno
weight: 200400
---

Doposud jsem užíval pojem "program" ale tento pojem v operačních systémech má specifický význam.

## Program, aplikace

"Program" potažmo "aplikace" jsou v kontextu OS soubory, které je možné **spustit**. Jinými slovy, jsou to někde uložené **instrukce pro procesor** které samy o sobě nic nedělají. Nejdřív je nutné instruovat OS aby program spustil.

Běžný český uživatel většinou používá OS Windows a v něm spouští program ve Windowsech (většinou dvojitým) poklepáním na nějakou ikonku.

{{< figure align=center src="../wowikona.png" title="Ikonka na ploše v operačním systému Windows" >}}


## Entry point

Při spuštění jakéhokoliv programu nejdřív OS najde kompatibilní **entry point** [^e] což je jinými slovy místo, kde pro daný program začínají instrukce, které mohou začít proudit do procesoru.

Entry point je standard **odlišný mezi různými OS**. Z tohoto důvodu není možné aplikaci na Windows spustit např. na macOS a naopak.

{{< figure align=center src="../entry-point.png" width=200 title="Entry point v programu" >}}

## Proces

Po nalezení entry pointu se pro program vytvoří nový **proces**. Proces je pouze něco jako evidenční záznam který shromažďuje důležité informace pro další věci, které se v rámci procesu dějí.

{{< figure align=center src="../program-proces.png" width=300 title="Program a proces" >}}

Proces však není to, co běží. Je to pouze záznam v paměti OS. To, co reálně běží je **thread**.

## Thread

Po nalezení entry pointu OS vytvoří pro proces **thread** [^t]. Tomuto prvnímu vláknu se vždycky říká **main thread**. [^m]

{{< figure align=center src="../main-thread.png" width=300 title="Hlavní vlákno" >}}

Vlákno je **přidělená kapacita procesoru pro zpracovávání instrukcí**.

Dále je důležité si zapamatovat, že:

- Vlákna jsou koncept až na vrstvě OS
- OS mají nad vlákny absolutní kontrolu
- OS zná všechna běžící vlákna a uchovává si informace o nich v paměti
- OS nikdy programům nesděluje jakou kapacitu procesoru vlákno dostalo
- Programy běžící pod OS nemohou vědět v jakém čase a s jakou kapacitou budou běžet 
- Z toho plyne, že reálně není možné vytvořit program pod OS, který by si nárokoval maximální čas procesoru na úkor ostatních procesů ale i na úkor OS samotného.

[^e]: *Česky snad "vstupní bod" ale obvykle se tento pojem nepřekládá.*
[^t]: *Česky "vlákno"*.
[^m]: *Česky "hlavní vlákno"*.