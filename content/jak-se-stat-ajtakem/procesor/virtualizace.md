---
draft: true
title: Virtualizace
weight: 715
---

Procesor může simulovat více procesorů (a komponent) najednou ale s každou přidanou simulací se sníží výkon všech ostatních „simulovaných“ procesorů. Tzn. pokud procesor simuluje 2 procesory tak každý z těchto „simulovaných“ procesorů, pokud bude zatížen na 100%, má ve výsledku maximálně 50% výkonu, než samotný procesor. Pokud simulujete 3 procesory tak každý má maximálně 33% výkonu atd. (pozn.: realita v moderních počítačích je složitější ale to není teď důležité).

To se ale nevztahuje pouze na procesory. Procesor  dokáže simulovat jakékoliv jiné zařízení a proto může klidně simulovat celý počítač nebo několik počítačů najednou. Tomu se říká virtualizace.

Dnešní procesory jsou tak výkonné, že na jednom moderním procesoru hravě zvládnete provozovat až desítku (byť slabších) dalších počítačů.

{{< figure align=center width=500 src="../virtualizace.png" title="Virtualizace" >}}

<div class="note1">

Váš běžný fyzický počítač dokáže simulovat nejspíš aspoň dva další počítače. Celkově tak můžete mít 3 počítače: 1 fyzický a 2 virtuální. Moderní procesory toto hravě zvládnou obsloužit. V IT je to (z mnoha důvodů) často využívaný mechanismus. Ještě se k tomuto tématu později vrátíme.

</div>

## Shrnutí

- Virtualizace je schopnost procesoru simulovat nejenom další procesory ale klidně i celé počítače s vlastními vstupy i výstupy.