---
draft: false
title: Frekvence a cyklus procesoru
weight: 70030
description: O tom, kolik času reálně zabírají běžící instrukce v procesorech
---

Moderní procesory mají frekvence mezi 2 až 5 GHz (gigahertz). 1 GHz znamená **jedna miliarda cyklů za vteřinu**. 

<div class="note-blue">

Jeden **cyklus procesoru** nebo také v angličtině jeden **tick** si můžete představit jako **jeden krok potřebný pro splnění nějaké instrukce**.

</div>

Na obrázku níže je příklad instrukce, která potřebuje 5 cyklů pro zpracování.

{{< figure align=center width=300 src="../cyklus.png" title="Cyklus procesoru" >}}

Různé instrukce vyžadují různý počet cyklů. Nejjednodušší logické instrukce odpovídají jednomu cyklu, složitější instrukce mohou zabrat i desítky ticků.