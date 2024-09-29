---
draft: true
title: Izolace OS
weight: 200200
---

Operační systém je program běžící přímo na počítači, tudíž má přístup ke všem komponentám.

Všechny ostatní programy běží v rámci operačního systému a tyto programy běžně **nemají ke komponentám přímý přístup**. Pokud tyto programy něco potřebují, přistupují k tomu **přes operační systém**.

{{< figure align=center width=500 src="../izolace.png" title="Izolace programů od počítače" >}}

Z [běžných komponent]({{< relref "../fyzicka-vrstva/komponenty" >}}) mají programy **zprostředkovaný přístup** pouze k:
- **procesoru** - bez přidělené kapacity procesoru by tyto programy nemohly ani běžet.
- **RAM paměti**
- **perzistentním uložištím**
- **síťovým kartám**
- **grafickým kartám**   