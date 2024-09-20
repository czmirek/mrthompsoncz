---
draft: false
title: Variabilní délka instrukce
weight: 70100
---

Moderní procesory nefungují na fixní délce instrukcí ale na **variabilní délce instrukce**. Instrukční sady `x86` a potažmo i `x86_64` podporují **proměnlivou délku instrukce** tzn. instrukce může mít délku mezi nějakým minimálním a maximálním počtem bitů. 

U `x86_64` je tento rozsah mezi mezi 8 až 120 bity přičemž některé instrukce umožňují seskupovat více instrukcí do sebe. V rámci spuštění jedné velké instrukce se tak provede více operací najednou.

Tyto komplexní detaily však běžný ajťák nezná a ani znát nepotřebuje.