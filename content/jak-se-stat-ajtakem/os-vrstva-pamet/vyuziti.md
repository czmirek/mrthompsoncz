---
draft: false
title: Využití persistentního uložiště
weight: 210200
---

**Virtuální paměť** však nevyužívá jen RAM paměť ale i **dostupné persistentní uložiště**. Zpravidla je to uložiště, na kterém je OS nainstalován, v běžných OS to lze nastavit.

{{< figure align=center width=500 src="../virtualmem2.png" title="Virtuální paměť" >}}

OS je však inteligentní a ví, že persistentní uložiště jsou **řádově pomalejší**. Využívání perzistentních uložišť běžící programy může rapidně zpomalit, proto se OS nejdřív snaží naplno využít dostupnou fyzickou RAM paměť.

**Kapacita virtuální paměti** není proto omezena kapacitou RAM pamětí ale společnou kapacitou RAM paměti a (nastavených) perzistentních uložišť.