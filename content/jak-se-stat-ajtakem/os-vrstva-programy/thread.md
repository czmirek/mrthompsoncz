---
draft: false
title: Thread
weight: 200700
---

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

[^t]: *Česky "vlákno"*.
[^m]: *Česky "hlavní vlákno"*.