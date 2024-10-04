---
draft: false
title: Stavy procesu
weight: 200800
---

OS u procesů eviduje jeho **stav**. Tyto stavy jsou napříč OS různé ale hodně se podobají.

Zpravidla jde o stavy:

- **Vytvořeno** --- OS právě proces spouští a ještě nebyla dokončena veškerá režie (např. načtení do RAM paměti) pro jeho skutečné spuštění
- **Čeká** --- proces je načtený v RAM paměti a čeká na přidělení času procesoru
- **Běží** --- proces běží v rámci OS normálně
- **Končí** --- proces se ukončuje