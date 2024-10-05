---
draft: false
title: Stavy procesu
weight: 200800
---

OS u procesů eviduje jeho **stav**. Tyto stavy jsou různé napříč různými OS ale lze identifikovat jakési základní stavy, které mají mezi různými OS víceméně stejný význam.

Zpravidla jde o stavy:

- **Vytvořeno** --- OS právě proces spouští a ještě nebyla dokončena veškerá režie (např. načtení do RAM paměti) pro jeho skutečné spuštění
- **Čeká** --- proces je načtený v RAM paměti a čeká na přidělení času procesoru
- **Běží** --- proces běží v rámci OS normálně
- **Končí** --- proces se právě ukončuje