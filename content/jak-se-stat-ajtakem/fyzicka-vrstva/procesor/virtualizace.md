---
draft: false
title: Virtualizace
weight: 253
---

Procesor může simulovat více procesorů (a komponent) najednou ale s každou přidanou simulací se sníží výkon všech ostatních „simulovaných“ procesorů. Tzn. pokud procesor simuluje 2 procesory tak každý z těchto „simulovaných“ procesorů, pokud bude zatížen na 100%, má ve výsledku maximálně 50% výkonu, než samotný procesor. Pokud simuluješ 3 procesory tak každý má maximálně 33% výkonu atd. (pozn.: realita v moderních počítačích je složitější ale to není teď důležité)

To se ale nevztahuje pouze na procesory. Procesor totiž dokáže simulovat jakékoliv jiné zařízení a proto může klidně simulovat celý počítač nebo několik počítačů najednou. Tomu se říká virtualizace.

Dnešní procesory jsou tak výkonné, že na jednom moderním procesoru hravě zvládnete provozovat až desítku (byť slabších) dalších počítačů!

![Virtualizace](/jak-se-stat-ajtakem/fyzicka-vrstva/procesor/virtualizace.png)

<div class="note1">

Tvůj fyzický počítač dokáže simulovat nejspíš aspoň dva další počítače a mít tak dohromady 3 počítače: 1 fyzický a 2 virtuální. Moderní procesory toto hravě zvládnou obsloužit. V IT je to často využívaný mechanismus. Ještě se k tomuto tématu později vrátíme.

</div>

## Shrnutí

- Virtualizace je schopnost procesoru simulovat nejenom další procesory ale klidně i celé počítače s vlastními vstupy i výstupy.