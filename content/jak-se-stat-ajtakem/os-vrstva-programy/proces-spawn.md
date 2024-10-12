---
draft: false
title: Proces spawn
weight: 201000
---

Jakýkoliv proces má schopnost spustit jiný program a nastartovat tedy další proces. Běžný uživatel zpravidla nepracuje s programy, které tuto schopnost využívají a pokud ano tak o tom ani neví.

Běžný ajťák by tomu ale měl rozumět více do detailu

## Parent + child

*(Parent + child = doslova rodič a dítě)*

Jakmile proces A nastartuje proces B tak pak platí, že:

- Proces A je parentem procesu B *(A je rodičem B)*
- Proces B je childem procesu A *(B je dítětem A)*

"Aktu" vytvoření procesu jiným procesem se také někdy říká "spawn" nebo "spawnutí" *(doslova "zplození")* procesu.