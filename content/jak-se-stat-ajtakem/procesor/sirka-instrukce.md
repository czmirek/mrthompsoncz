---
draft: false
title: Šířka instrukce
weight: 70020
description: O šířce instrukce v procesorech
---

**Šířka instrukce** je **počet bitů v instrukci**. 

<div class="note-blue">

Každý procesor je vyrobený na pevnou šířku instrukce. [^s] Instrukce nemůže obsahovat více ani méně bitů, než kolik je šířka instrukce. Toto je jednoduše odraz fyzické reality. 6-bitový procesor je 6-bitový, protože na vstupu do něj reálně vede [6 fyzických drátů]({{< relref "instrukce" >}}).

</div>

{{< figure align=center width=300 src="../sirka-instrukce.png" title="Vstupní instrukce procesoru" >}}


[^s]: *Realita je trochu složitější. Moderní procesory umí zpracovávat zanořené instrukce, které mají variabilní (=libovolnou) délku, to ale není pro běžného ajťáka podstatné.*