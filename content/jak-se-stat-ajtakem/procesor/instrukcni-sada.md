---
draft: false
title: Instrukční sada
weight: 70080
---

Instrukční sada je **předepsaná norma** podle které je procesor vyrobený a s tím souvisí i jaké instrukce podporuje a jak se tyto instrukce chovají.

Moderní a běžné instrukčnísady jsou:

- `x86` – starší počítače a procesory.
  - Šířka instrukce: 32
- `x86-64` (nebo jen `x64`) – rozšíření x86, prakticky ve všech počítačích, notebocích a serverech všude na světě.
  - Šířka instrukce: 64
- `ARM` – mobilní telefony a tablety
  - Šířka instrukce: 32 a 64 (ARM64)

⚠️ **Některé instrukční sady lze zaměnit, některé ne.**

- `x86` program **nebude** běžet na `ARM` a naopak
- `x86_64` program **nebude** běžet na `ARM` a naopak
- `x86` program **bude** běžet na `x86_64` ale ne naopak

## Proč je tak málo instrukčních sad?

- **Obrovská složitost**: moderní instrukční sady jsou obrovsky komplexní protože vznikly už hodně dávno a neustále se modifikovaly. Instrukční sada `x86` vznikla v roce 1978. [^z]

- **Zpětná kompatibilita**: Instrukční sada `x86` je kritizována za spoustu historických přešlapů se kterými už ale nelze nic dělat. Proč? Protože celý IT svět je víceméně na `x86` postavený.

[^z]: Oficiální dokumentace k x86-64 má [2198 stránek](https://www.intel.com/content/dam/www/public/us/en/documents/manuals/64-ia-32-architectures-software-developer-instruction-set-reference-manual-325383.pdf) a k ARM64 má [8538 stránek](https://www.intel.com/content/dam/www/public/us/en/documents/manuals/64-ia-32-architectures-software-developer-instruction-set-reference-manual-325383.pdf)
