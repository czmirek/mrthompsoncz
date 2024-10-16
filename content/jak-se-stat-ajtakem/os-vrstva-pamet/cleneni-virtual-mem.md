---
draft: false
title: Členění virtuální paměti
weight: 210400
---

OS rozděluje virtuální paměť na dvě části:

- **kernel space**: chráněná část, ve které běží operační systém a všechny jeho interní procesy a mechanismy.
- **user space**: v této části běží všechny ostatní procesy, zejména programy spuštěné uživatelem

{{< figure align=center width=500 src="../memspace.png" title="Rozdělení virtuální paměti" >}}

OS se snaží zabírat co nejmenší prostor aby zbytek prostoru virtuální paměti byl dostupný pro uživatelské účely.
