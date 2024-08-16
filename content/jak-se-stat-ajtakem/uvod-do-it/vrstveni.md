---
draft: false
title: Vrstvy IT
weight: 130
---

Moderní počítače jsou extrémně komplexní a komplikovaná zařízení. Z toho důvodu se nesnažíme pochopit počítač jako celek a místo toho zkoumáme jeho jednotlivé **vrstvy**.

Podle těchto vrstev je víceméně psán i tento návod. Kvalitní ajťák by těmto vrstvám měl dobře rozumět a proto jim bude věnována patřičná pozornost.

## Hardware vrstva

- **Fyzická vrstva** = reálná fyzická zařízení, kterých se můžete dotknout.
- **Elektronická vrstva** = elektřina putující v těchto fyzických zařízeních
- **Signální vrstva** = signály, která jsou elektřinou reprezentovány
- **Binární vrstva** = kódování, které je reprezentované signály
- **Binární aritmetika** = matematické operace, které lze provádět díky binární vrstvě
  - *Celočíselná reprezentace* = jak jsou v binární vrstvě reprezentována celá čísla
  - *Desetinná reprezentace* = jako jsou v binární vrstvě reprezentována desetinná čísla
  - *Písmena / znaky* = jako jsou v binární vrstvě reprezentována písmena

## Software vrstva
- **Bare-metal/embedded software** = software běžící přímo "na železe" bez operačního systému (nebo váš vlastní operační systém).
- **Operační systém** = software sjednocující obrovskou složitost a rozdílnost hardwaru do jednoho uživatelského rozhraní
- **Software** = software běžící v rámci nějakého operačního systému. Tento návod je zaměřený na "běžné" ajťáky kteří píší software na této vrstvě. Na této úrovni je (dle mého názoru) psáno 90% veškerého softwaru na světě.

## Ilustrace

{{< figure align=center width=600 src="/jak-se-stat-ajtakem/uvod-do-it/vrstvy.png" title="Vrstvy IT" >}}