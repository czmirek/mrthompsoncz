---
draft: false
title: Vrstvy IT
weight: 130
---

Moderní počítače jsou extrémně komplexní zařízení. Z toho důvodu se nesnažíme pochopit počítač jako celek a místo toho zkoumáme jeho jednotlivé **vrstvy**. Podle těchto vrstev je víceméně psán i tento návod. 

Každý ajťák by těmto vrstvám měl dobře rozumět a proto jim bude věnována patřičná pozornost.

## Hardware vrstva

- **Fyzická vrstva** = reálná fyzická zařízení
- **Elektronická vrstva** = elektřina putující v těchto fyzických zařízeních
- **Signální vrstva** = signály, která jsou elektřinou reprezentovány
- **Bitová vrstva** = kódování, které je reprezentované signály
- **Bitové interpretace** = různá kódování, která jsou reprezentovaná bity 
  - **Bajty** = kódování reprezentované bity
  - **Čísla** = kódování reprezentující čísla
    - *Celočíselná interpretace* = jak jsou v binární vrstvě reprezentována celá čísla
    - *Desetinná interpretace* = jako jsou v binární vrstvě reprezentována desetinná čísla  
  - **Binární aritmetika** = matematické operace (sčítání, odčítání, násobení, dělení, atd.), které lze provádět díky bitové vrstvě
  - **Znakové sady** = jak jsou v bitové vrstvě reprezentována písmena 


## Software vrstva
- **Bare-metal/embedded software** = software běžící přímo "na železe". Tento software je běžný u "specializovaných počítačů" jako jsou chytré domácnosti, řídící jednotky v automobilech a podobně.
- **Operační systém** = software sjednocující obrovskou složitost a rozdílnost hardwaru v počítačích do jednoho uživatelského rozhraní.
- **Běžný software** = software běžící v rámci operačního systému. Tento návod je zaměřený na "běžné" ajťáky kteří píší software na této vrstvě. Na této úrovni je (dle mého názoru) psáno 90% veškerého softwaru na světě.

## Ilustrace vrstev

{{< figure align=center width=600 src="../vrstvy2.png" title="Vrstvy IT" >}}