---
draft: true
title: Izolovaný OS
weight: 200200
---

Operační systém je **izolovaný** od programů, které se v něm spouští a to jak na úrovni **instrukcí pro procesor** tak i na úrovni **RAM paměti**.

- U **instrukcí pro procesor** je tato izolace dosažena využitím **procesorových režimů** kterou všechny moderní procesory podporují.  

- U **RAM paměti** je tato izolace dosažena jednoduše zablokováním možnosti přímého přístupu do RAM paměti. Pro získání kapacity do paměti musí jakýkoliv program **zažádat operační systém o kapacitu paměti**.

Obojí popíšu v následujících kapitolách.