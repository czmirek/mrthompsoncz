---
draft: false
title: Virtuální pamět
weight: 520
---

## Kernel space a User space

Procesor s RAM* pamětí interaguje velice rychle a stahuje z ní instrukce, které má rozeběhnout: toto jsou instrukce jak OS tak i softwaru, který pod OS běží.

Proto OS dělí paměť na dvě části:

- Kernel space: toto je prostor OS a nikoho jiného
- User space: zde je veškerý ostatní software
  - Každá aplikace zároveň vidí pouze svoji vlastní paměť a zpravidla nemůže zapisovat do paměti jiných aplikací.

Do kernel space má přístup jen operační systém, žádný jiný software se do tohoto prostoru paměti nedostane.

<div class="note1">

Co je RAM? Anglicky „Random Access Memory“ neboli „Paměť náhodného přístupu“. To znamená, že každý bit nebo bajt má svoji vlastní adresu a pomocí této adresy přečtete obsah na dané adrese ihned.

Existují i jiné typy pamětí, například „SAM“ (kde „S“ znamená Sekvenční) což je třeba stará filmová páska. Pokud chcete v nějakém přehrávači na filmovou pásku vidět konkrétní část filmu, musíte celý film „přetočit“ na dané místo.

</div>

## Virtuální paměť

Aplikace a software běžící v OS vůbec na prostor v RAM paměti nevidí. OS zprostředkovává každé aplikaci virtuální paměť což je z pohledu aplikace „neomezený“ prostor který tady někde plave ve vzduchu a software má naprostou svobodu v množství paměti, kterou spotřebuje.

Aby se aplikace vůbec k paměti dostaly tak OS nabízí tyto dvě základní funkce:

- dej mi bajty z virtuální paměti
- vem si bajty zpátky

![Virtuální pamět](/jak-se-stat-ajtakem/os-vrstva/virtual-mem.png)

## Paging / swapping

Software má naprosto svobodu v tom, kolik paměti využije. Operační systém nemá vůbec žádný názor na to, kolik paměti jaká aplikace potřebuje, OS je jenom zprostředkovatel. Některé aplikace potřebují víc paměti, některé méně, některé aplikace potřebují někdy více, někdy méně. Záleží, na co počítač používáš.

RAM paměť však není omezená. Když programátor tvoří software, musí si dát pozor, aby jeho software nevyužíval více paměti, než kolik doopravdy potřebuje.

Co se stane, když RAM paměť dojde? OS provádí tzv. paging což znamená, že OS začne přehazovat malé bloky dat mezi RAM pamětí a nějakým jiným avšak většinou podstatně pomalejším úložištěm než je RAM paměť jako je HDD/SSD.

Jakmile začne docházet k pagingu, uživatel to citelně pozná – počítač se začne „kousat“ a práce s ním začne být nesnesitelná. Zahlcení RAM paměti má samozřejmě vliv i na ostatní procesy.

Swapping je pojmenování pro starší, již nepoužívaný způsob přehazování celých procesů (ne jen jejich dílčích bloků) mezi RAM a jiným uložištěm, zmiňuji se o tom, že se tento pojem používá dodnes i když moderní PC už swapping nedělají.

## Shrnutí

- OS dělí RAM paměť na dvě části: kernel space a user space
- Kernel space je prostor paměti, ve které se nachází operační systém
- User space je prostor paměti, ve které se nachází běžící aplikace.
- Aplikace běžící v OS vidí pouze svoji vlastní paměť a do kernel space nebo do user space jiných aplikací nevidí
- Virtuální paměť je způsob, jakým OS zprostředkovává paměť jednotlivým aplikacím.
- Aplikace mají možnost rezervovat si pro sebe bajty z paměti a nebo tyto bajty vrátit
- Aplikace jsou zodpovědné za množství paměti, se kterým pracují
- Paging je způsob, jakým se OS vypořádává s nedostatkem RAM paměti přehazováním datových bloků mezi RAM a jiným úložištěm jako HDD/SSD