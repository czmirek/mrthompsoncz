---
draft: false
title: Aplikace / program / software
weight: 774
---

Všechny moderní procesory fungují na stejném principu, jako před 50 lety.

### **Krok 1:** 

Nějakým způsobem jsou někam připraveny instrukce.

U moderních počítačů jsou instrukce připraveny do RAM paměti.

### **Krok 2:** 

Procesor čte instrukce **jednu po druhé až do konce**.

# Co je software?

Software / program / aplikace --- ať už to nazveme jakkoliv [^b] --- z pohledu bitové vrstvy není nic jiného než **nějaký seznam instrukcí**.

Běžný uživatel - a v mém pojetí i běžný ajťák - má ve svém počítači na disku připravený **operační systém**. Toto je z bitového pohledu aplikace, jako každá jiná - pouze seznam instrukcí, který se nahraje do RAM paměti a procesor tyto instrukce začne provádět, jednu po druhé, až do konce.

## Pro operační systém nedoběhne až do konce?

Což vede k otázce: pokud procesor čte instrukce jednu po druhé až do konce, jak je možné, že se operační po spuštění ihned nevypne?

Tomu už také dokážeme porozumět. Instrukce operačního systému se totiž točí ve smyčce (viz. [JUMP instrukce]({{< ref "ridici-instrukce" >}})). Operační systém je naprogramovaný tak, že v této smyčce se točí do té doby, dokud mu to uživatel (nebo jiný mechanismus) neřekne. Jakmile uživatel takovou instrukci zadá, operační systém z této smyčky vystoupí a spustí se instrukce které zaúkolují základní desku, aby počítač vypla.

[^b]: *Neexistuje žádná oficiální nebo formální definice toho, co v IT znamená software, aplikace nebo program. Pojmenovávání čehokoliv v IT je jedna z nejobtížnějších věcí v IT vůbec.*