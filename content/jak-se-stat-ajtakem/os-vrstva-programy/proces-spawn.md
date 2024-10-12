---
draft: false
title: Proces spawn
weight: 201000
---

Jakýkoliv proces má schopnost spustit jiný program a nastartovat tedy další proces. Běžný uživatel zpravidla nepracuje s programy, které tuto schopnost využívají a pokud ano tak o tom ani neví.

## Parent + child

*(Parent + child = doslova rodič a dítě)*

Jakmile proces A nastartuje proces B tak pak platí, že:

- Proces A je parentem procesu B *(A je rodičem B)*
- Proces B je childem procesu A *(B je dítětem A)*

"Aktu" vytvoření procesu jiným procesem se také někdy říká "spawn" nebo "spawnutí" *(doslova "zplození")* procesu.

## Specifika v OS

- V Linuxových distribucích/macOS mají tyto vztahy význam.
  - Ukončení rodičovského procesu normálně ukončí i dětské procesy
  - Chybné ukončení rodičovského procesu může zanechat *sirotky*.
  - Chybné ukončení dětského procesu může zanechat *zombie*.
  
- Ve Windows OS žádné rodičovské-dětské vztahy mezi procesy neexistují. Jakákoliv taková označení jsou jen na oko.
  - Zabití "rodičovského" procesu nemá žádný vliv na jiné procesy.
  - Jakékoliv "dětské" procesy jsou na svém rodičovském procesu absolutně nezávislé.