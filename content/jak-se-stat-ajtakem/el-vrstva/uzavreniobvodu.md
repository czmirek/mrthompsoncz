---
draft: false
title: Uzavření obvodu
weight: 302
description: Co je uzavření obvodu v počítačích, jaké všechny obvody se v počítačích nachází a co to znamená pro běžného ajťáka
---

Aby elektřina mohla v obvodu putovat, musí být obvod **uzavřený**. Nejlépe se to ilustruje na diagramu obyčejné lampčiky s vypínačem.

Kabel od lampičky který zapojujete do zásuvky obsahuje dva menší kabely - v češtině se jim říká *fáze* a *nulový obvod*. Elektřina putuje [^1] po kabelu z fáze do nulového obvodu. Pokud nulový obvod není připojený, elektřina neputuje. Když lampičku vypnete, obvod je přerušený. Když ji zapnete, obvod je uzavřený.

{{< figure align=center width=500 src="../lampicka.png" title="Elektrické schéma lampičky" >}}

Běžný počítač není v tomto ohledu odlišný. Aby elektřina skrz něj proudila, musí být uzavřený obvod.

{{< figure align=center width=300 src="../schemapc.png" title="Elektrické schéma zapojeného PC" >}}

Uprostřed počítače má téměř každá komponenta **svůj vlastní obvod**. Aby mohla komponenta fungovat, musí být za provozu každý obvod **uzavřený**.

{{< figure align=center width=300 src="../kombobvody.png" title="Kombinované obvody" >}}

Některé komponenty mohou mít **více nezávislých obvodů**.

## Co z toho plyne pro běžného ajťáka?

- Běžný ajťák se nezabývá schématy obvodů. To je věc pro elektrotechniky.
- Pokud je jakákoliv komponenta viditelně fyzicky poškozena, téměř určitě došlo k přerušení obvodu = komponenta je nenávratně zničena a lze ji vyhodit.
- Viditelně poškozenou komponentu do počítače **nikdy nezapojujeme** - může dojít k poškození ostatních komponent.
- Zapojování komponent do počítače děláme **jen na počítači který je odpojený od elektřiny!** 

[^1]: *Putující elektřina v obvodu jsou ve skutečnosti dvě věci: elektrony (částice) putující skrz atomy vodiče a elektromagnetické pole které okolo vodiče vzniká. Zatímco elektrony putují skrz vodič relativně pomalu (1 milimetr za vteřinu) tak elektromagnetické pole putuje obvodem rychlostí světla.*