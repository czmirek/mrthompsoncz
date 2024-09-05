---
draft: false
title: Přerušení
weight: 704
---

Jakmile zapnete počítač, procesor společně se základní deskou hledá místo, odkud začít číst instrukce. Tyto první instrukce reprezentují většinou nějaký operační systém jako je například Windows nebo Linux.

Do procesoru se může kdykoliv dostat instrukce přerušení (anglicky „interrupt“) která tok instrukcí přeruší jiným tokem instrukcí. Jakmile je tok instrukcí dokončen, naváže procesor na předchozí tok.

K čemu je toto dobré?

Pohněte ukazatelem myši. Gratuluji – právě v procesoru došlo k přerušení. Počítač zpracoval fyzické signály z myši přímo v procesoru, došlo k přerušení díky kterému se na obrazovce tvého počítače posunul kurzor. Procesor pak pokračoval dál v předchozím toku instrukcí.

Přerušení se v procesorech využívá pro zpracování vstupů, využívá se ale i pro pokročilejší programování, o tom si povíme později.

## Shrnutí

- Přerušení je instrukce do procesoru, která přeruší současný tok instrukcí jiným tokem instrukcí a procesor musí toto přerušení zpracovat.
- Přerušení proběhne například při použití klávesnice nebo myši.