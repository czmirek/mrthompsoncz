---
draft: false
title: Sériové zpracování instrukce
weight: 70021
description: O tom, jak procesory zpracovávají instrukce jednu za druhou.
---

<div class="note-blue">

⚠️ **Důležité k zapamatování**: Procesory zpracovávají instrukce **sériově** tedy jednu za druhou. Procesor [^c] neumí zpracovávat instrukce paralelně. [^p]

</div>

{{< figure align=center src="../seriove-zpracovani.png" title="Sériové zpracování instrukcí" >}}

Obrázek výše je doufám dostatečně názorný.

- Právě se zpracovává nějaká instrukce 110011
- Po zpracování této instrukce se začne zpracovávat instrukce 2. v pořadí tedy 111100
- Následuje instrukce 000111
- Pak 010001
- Pak 101100
- Atd.


[^c]: *Respektive procesorové jádro, o tom budu mluvit později.*

[^p]: *U moderních procesorů to není 100% pravda ale to není pro běžného ajťáka podstatné. O moderních procesorech pojednává [samostatný článek]({{< relref "hw-slozitosti" >}}) později.*