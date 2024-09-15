---
draft: false
title: Variabilní délka instrukce
weight: 710
---

Doposud jsem v tomto návodu mluvil o tom, že procesory mají **fixní délku instrukce** např. 32 nebo 64 bitů.

Realita je bohužel složitější. Instrukční sady `x86` a potažmo i `x86_64` mají **proměnlivou délku instrukce** tzn. instrukce může mít délku mezi nějakým minimálním a maximálním počtem bitů. 

U `x86_64` je tento rozsah mezi mezi 8 až 120 bity přičemž některé instrukce umožňují seskupovat více instrukcí do sebe tzn. v rámci spuštění jedné velké instrukce se provede více operací najednou.

Tyto komplexní detaily však běžný ajťák znát nemusí.