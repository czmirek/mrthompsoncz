---
draft: false
title: Co je operační systém (OS)
weight: 100100
---

Operační systémy jsou programy, jejichž hlavním účelem je **zjednodušit práci s počítačem pro běžného uživatele** ale i pro běžného ajťáka v mém pojetí.

OS toto dělají několika způsoby.

### 1. Schovávají obrovskou složitost hardwaru na bitové vrstvě

Většinu běžných uživatelů nezajímá *"co se děje pod poklicí"* tedy co se reálně děje v hardwaru na bitové vrstvě.

Běžný ajťák by dle mého názoru měl [vědět trochu víc]({{< relref "../procesor" >}}) ale pouze až do nějaké úrovně detailu, kde to [dává smysl]({{< relref "../procesor/hw-slozitosti" >}}).

Běžný ajťák v mém pojetí totiž, stejně jako běžný uživatel, pracuje na úrovni operačního systému.

### 2. Fungují stejně napříč odlišně vyrobenými komponentami

OS nás zbavují komplikací spojené s různými komplikovanými protokoly, standardy, systémy a subsystémy které se mohou lišit v rámci jednoho typu komponenty, například u základní desky.

Základní deska může fungovat různě:

- mezi různými výrobci komponent
- mezi různými modely jedné komponenty
- mezi různými výrobními sériemi v rámci jednoho modelu
- mezi různými roky v rámci jedné vyrobené série
- atd.

OS toto všechno znají a jsou na to připravené.

### 3. Umožňují instalovat a spouštět programy

S moderním počítačem se nemusí pracovat stejně jako na konci 60., 70. let 20. století. Nemusíte se zabývat tím, že na procesorovém jádře můžete reálně rozeběhnout [pouze jeden program]({{< relref "../procesor/jediny-program"  >}}).

Díky OS můžete na počítač nainstalovat a spustit libovolné množství programů. [^m]

### 4. Vytváří nad počítačem úplně novou vrstvu

Tento bod není důležitý pro běžného *uživatele* ale je naprosto klíčový pro **běžného ajťáka** který musí OS vrstvě velmi dobře rozumět.

[^m]: *A běžný ajťák by měl rozumět, jak to OS dělají. Toto popisuji v pozdější kapitole.*