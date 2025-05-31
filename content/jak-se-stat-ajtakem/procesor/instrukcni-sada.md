---
draft: false
title: Instrukční sada
weight: 70080
description: Instrukční sada je předepsaná norma instrukcí pro procesory.
---

Instrukční sada je **předepsaná norma instrukcí** která určuje, jaké instrukce musí procesor podporovat a jak se tyto instrukce mají v procesoru chovat.

<div class="note-blue">

⚠️ **Důležité k zapamatování**: Každý procesor je vyrobený pro jednu konkrétní instrukční sadu. Procesory podporující více instrukčních sad se nevyrábí.

</div>

Mezi moderní a běžné instrukční sady patří:

- `x86` – starší počítače a procesory. 32 bitové instrukce.
- `x86-64` (nebo jen `x64`) – rozšíření x86, prakticky ve všech počítačích, notebocích a serverech všude na světě. 64 bitové instrukce.
- `ARM` – mobilní telefony a tablety. Podvarianty ARM podporují buď 32 nebo 64 bitové instrukce.

⚠️ **Některé instrukční sady lze zaměnit, některé ne.**

- `x86` program **nebude** běžet na `ARM` a naopak
- `x86_64` program **nebude** běžet na `ARM` a naopak
- `x86` program **bude** běžet na `x86_64` ale ne naopak

## Proč je tak málo instrukčních sad?

- **Obrovská složitost**: moderní instrukční sady jsou obrovsky komplexní protože vznikly už hodně dávno a neustále se modifikovaly a vylepšovaly. Instrukční sada `x86` vznikla v roce 1978 a používá se dodnes. [^z]

- **Zpětná kompatibilita**: Instrukční sada `x86` je kritizována za spoustu historických přešlapů se kterými už nelze nic moc dělat, protože celý moderní IT svět je na `x86` postavený.

[^z]: *Oficiální dokumentace k x86-64 má [2198 stránek](https://www.intel.com/content/dam/www/public/us/en/documents/manuals/64-ia-32-architectures-software-developer-instruction-set-reference-manual-325383.pdf) a k ARM64 má [8538 stránek](https://www.intel.com/content/dam/www/public/us/en/documents/manuals/64-ia-32-architectures-software-developer-instruction-set-reference-manual-325383.pdf)*