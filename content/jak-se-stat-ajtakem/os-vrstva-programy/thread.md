---
draft: false
title: Vlákno
weight: 200700
---

Po nalezení entry pointu OS vytvoří pro proces **thread**, česky vlákno. Prvnímu vláknu procesu se vždy říká **main thread** nebo hlavní vlákno.

{{< figure align=center src="../main-thread.png" width=300 title="Hlavní vlákno" >}}

Vlákno je **přidělená kapacita procesoru pro zpracovávání instrukcí**. Dá se říct, že vlákno už reálně reprezentuje *nějaké operace* které se provádí od začátku až do konce. Není to nic jiného, než CPU prováděné instrukce.

{{< figure align=center src="../instrukce-vlakna.png" width=500 title="Běžící vlákno" >}}

⚠️ **Důležité k zapamatování**: Jakmile skončí hlavní vlákno procesu, **skončí celý proces**.