---
draft: false
title: Proces child/parent
weight: 201000
---

Jakýkoliv proces má schopnost spustit jiný program a nastartovat tedy další proces. Běžný uživatel zpravidla nepracuje s programy, které tuto schopnost využívají a pokud ano tak o tom ani neví.

Běžný ajťák by tomu ale měl rozumět více do detailu

## Parent + child [^p]

Jakmile proces A nastartuje proces B tak pak platí, že:

- Proces A je parentem procesu B [^a]
- Proces B je childem procesu A [^b]

"Aktu" vytvoření procesu jiným procesem se také někdy říká "spawn"[^s] nebo "spawnutí" procesu.

## Zabití procesu procesem

OS dovoluje procesům spawnovat ale i zabíjet jiné procesy. Např. procesy, které sám spawnoval. [^k]

[^p]: *Doslova "rodič + dítě"*
[^a]: *Doslova proces A je rodičem procesu B*
[^b]: *Doslova proces B je potomkem procesu A*
[^s]: *Doslova "zplození"*
[^k]: *Pak z toho vznikají takové veselé věty jako třeba "parent kills child" neboli "rodič zabil dítě"*