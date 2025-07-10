---
draft: true
title: Zjednodušený bitový model
weight: 70990
---

Tato kapitola je shrnutí všech důležitých informací z kapitol o procesoru.

{{< figure align=center width=700 src="../zjednoduseny-model.png" title="Zjednodušený pohled na bitovou vrstvu moderního PC" >}}

- **Procesor je srdcem i mozkem celého počítače.** Instrukcemi rozhoduje o každém bitu v počítači.
- **Procesor se řídí tokem instrukcí z RAM paměti.** 
  - U moderních multijádrových procesorů se každé jádro může řídit svým vlastním tokem instrukcí z RAM paměti
  
- Instrukce CPU se dělí na tyto **3 typy**:
  - **datové**: těmito instrukcemi procesor přikazuje, kam se který bit má přesunout
  - **aritmeticko-logické**: těmito instrukcemi procesor bity matematicky či logicky transformuje
  - **řídící**: těmito instrukcemi procesor mění tok instrukcí
- **Podrutina/funkce** je opakovaně přepoužitelný seznam instrukcí se vstupními parametry a **jedním** výstupním parametrem.
- **Calling convention** je konvence určující jak se má s podrutinami pracovat.
- **Hardwarové přerušení** je proces, kdy je možné jakoukoliv jinou komponentou v počítači ovlivnit právě probíhající tok instrukcí. CPU podle přerušení zavolá nějakou funkci (podrutinu) a až ji vykoná, vrátí se zpět k normálnímu toku instrukcí.
- **Softwarové přerušení** je situace, kdy nějaká instrukce, úmyslně či neúmyslně, vyvolá v procesoru přerušení a ovlivní tak tok instrukcí. CPU podle přerušení zavolá nějakou funkci (podrutinu) a až ji vykoná, vrátí se zpět k normálnímu toku instrukcí.
- **Synchronní I/O**: Procesor je schopný přímo komunikovat s jakýmkoliv zařízením v systému, zpravidla to ale nedělá jelikož tato zařízení jsou téměř vždy řádově pomalejší, než samotný procesor.
- **Asynchronní I/O**: Procesor komunikuje s ostatními zařízeními nepřímo. Instruuje chipset základní desky, aby data, která je potřeba přečíst, přesunul do RAM paměti nebo pro zápis aby je z RAM paměti převzal.
  - Jakmile je operace hotová, chipset základní desky (potažmo související komponenta) notifikuje procesor o dokončení této operace pomocí **hardwarového přerušení**.
