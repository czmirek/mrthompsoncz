---
draft: false
title: Program
weight: 70740
---

Všechny moderní procesory fungují na stejném principu jako před 70 lety.

### **Krok 1:** 

*Nějakým způsobem* [^z] jsou *odněkud* [^o] zkopírovány instrukce do RAM paměti.

### **Krok 2:** 

Procesor čte připravené instrukce **jednu po druhé až do konce**.

## Co je program?

Program (nebo software, nebo aplikace, ať už to nazveme jakkoliv [^b]) z pohledu bitové vrstvy není nic jiného než **nějaký seznam instrukcí**.

{{< figure align=center width=200 src="../program.png" title="Program = seznam instrukcí" >}}

Běžný uživatel - a v mém pojetí i běžný ajťák - má ve svém počítači na disku připravený **operační systém** a nikdy nepřipravuje programy **napřímo pro procesor**. [^k] 

**⚠️ Důležité k zapamatování**: běžný ajťák je schopný připravovat programy až na úrovni OS. V rámci této kapitoly se ještě nepohybujeme na úrovni OS.

[^z]: *U moderních počítačů je toto podrobněji popsáno v pozdější kapitole [BIOS/UEFI]({{< relref "bios-uefi" >}})*
[^o]: *Z perzistentního uložiště jako SSD, HDD nebo flash.* 
[^b]: *Neexistuje žádná oficiální nebo formální definice toho, co v IT znamená software, aplikace nebo program, tato slova jsou téměř vždy zaměnitelná. Pojmenovávání čehokoliv v IT je jedna z nejobtížnějších věcí vůbec.*
[^k]: *Toto popisuji později v kapitole [bare-metal programming]({{< relref "../os-vrstva-bit/bare-metal-programming" >}})*