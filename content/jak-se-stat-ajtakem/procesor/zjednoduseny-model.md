---
draft: false
title: Zjednodušený bitový model
weight: 799
---

Tato kapitola je shrnutí, čemu je důležité na bitové vrstvě rozumět.

{{< figure align=center width=700 src="../zjednoduseny-model.png" title="Zjednodušený pohled na bitovou vrstvu moderního PC" >}}

-  Procesor je srdcem i mozkem celého počítače. Instrukcemi rozhoduje o každém bitu v počítači.
-  Procesor se řídí jedním tokem instrukcí z RAM paměti. 
    - Nejspíš by dokázal se řídit instrukcemi z jiného zařízení ale kvůli obrovskému rozdílu mezi rychlostmi by nebyl efektivní.
    - U moderních multijádrových procesorů se každé jádro může řídit svým vlastním tokem instrukcí z RAM paměti
-  RAM paměť dokáže fungovat na vysokých frekvencích a proto je mezi procesorem a RAM pamětí dedikovaný kanál.

- Procesor v počítači dělá jen 3 typy instrukcí:
  - **datové**: těmito instrukcemi procesor přikazuje, kam se který bit má přesunout
  - **aritmeticko-logické**: těmito instrukcemi procesor bity matematicky či logicky transformuje
  - **řídící**: těmito instrukcemi procesor mění tok instrukcí
- Přerušení je proces, kdy je možné jakoukoliv jinou komponentou v počítači ovlivnit právě probíhající tok instrukcí. Program v RAM paměti ale musí být na takové přerušení připraven, jinak je přerušení ignorováno.
- Procesor je schopný přímo komunikovat s jakýmkoliv zařízením v systému, zpravidla to ale nedělá jelikož tato zařízení jsou téměř vždy řádově pomalejší, než samotný procesor.
- Procesor komunikuje s ostatními zařízeními nepřímo. Instruuje chipset základní desky, aby data, která je potřeba přečíst, přesunul do RAM paměti nebo pro zápis aby je z RAM paměti převzal.
  - Jakmile je operace hotová, chipset základní desky (potažmo související komponenta) notifikuje procesor o dokončení této operace pomocí přerušení.
