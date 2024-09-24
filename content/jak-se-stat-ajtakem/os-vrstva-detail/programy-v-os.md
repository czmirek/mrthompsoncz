---
draft: true
title: Programy pod OS
weight: 200100
---

Operační systémy umožňují **spouštět další programy**.

Tyto programy **nejsou odlišné od samotného OS** v tom významu, že jde pořád o **instrukce pro procesor** které se musí načíst do **RAM paměti** aby tyto instrukce bylo možné v procesoru zpracovat.

{{< figure align=center width=300 src="../programy-v-os.png" title="Programy v OS" >}}

## Z toho plynou otázky

1. Co když se jakýkoliv program pokusí změnit instrukce, které patří OS? Nezapomeňte na to, že procesor má plný přístup k RAM paměti a [může si sám za pochodu instrukce měnit]({{< relref "../procesor/instrukce-v-ram">}}).

2. Co když se jakýkoliv program pokusí změnit konfiguraci nějaké fyzické komponenty v počítači, kterou OS už nějakým způsobem nastavil? Nezapomeňte, že procesor má **plný přístup ke všem komponentám v počítači**.

3. Jak to OS dělá, že umožňuje, aby souběžně běžel jak OS tak i další, libovolné množství programů?