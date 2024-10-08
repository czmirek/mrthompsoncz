---
draft: false
title: Znakové sady
weight: 7110
---

**Znaková sada** je nějaká bitová interpretace normálních písmen a znaků.

Historicky existuje spousta znakových sad, zásadní jsou však jen některé.

## ASCII

Nejznámější a nejstarší znaková sada se jmenuje ASCII. Je důležité ji znát. Běžný počítačový uživatel na ní nejspíš nenarazí ale rodící se ajťák dřív nebo později ano.

A i kdyby ne, stejně je důležité ji znát, protože všechny důležité znakové sady vychází právě z ASCII.

Tato znaková sada se zapisuje na 8 bitů. (Historicky to bylo 7 bitů jako základ pro angličtinu a 8 bitů pro rozšířené znaky jakéhokoliv jiného jazyka, tato vlastnost se ale už nikde nepoužívá).


{{< figure align=center width=700 src="../ascii.png" title="ASCII" >}}

Velké `A` je číslo 65 což je v bitech `1000001`, malé `a` je 97 a podobně.

ASCII je velmi stará znaková sada (1963). Spoustu těch znaků v rozsahu 0 až 31 původně reprezentovala různé divné stavy, táhla, spínače, tlačítka, světýlka a pípátka které tehdejší počítače měly.

Dnes už mají počítače USB klávesnici a myš. Klávesnice předává informace úplně jiným kódem [^u] který se znakovými sadami nijak nesouvisí.

## Unicode

Jak počítače začalo používat mnohem víc lidí všude po světě, začaly vznikat další jazykové sady pro mnoho různých jazyků. Samotné ASCII neumí české znaky jako "ř" nebo "ň", pouze anglickou abecedu.

Kdysi byl ve znakových sadách dost bordel. Pro různé jazyky vznikaly různé znakové sady. Toto období naštěstí skončilo protože všichni začali používat **Unicode** což je název organizace která vymyslela znaková sadu se stejným názvem, která má 32 bitový rozsah. 

Už víte, že 32 bitů je 2<sup>32</sup> a to je 4294967296 — 4 miliardy možných znaků.

To je víc znaků, než kolik celé lidstvo vůbec vymyslelo za celou svoji existenci. 

Do 4 miliard se vejdou všechny abecedy světa, všechny symboly jazyků jako čínština které obsahují tisíce různých znaků, dále tam dostanete i všechny možné historické znaky, různé varianty různých znaků, dokonce i fiktivní, vymyšlené abecedy...a to jste pořád někde na čísle 100000? 200000? Pořád máte 4 miliardový nevyužitý prostor.

Ano, **emoji** nejsou nic jiného, než znaky ve znakové sadě Unicode.

## UTF-8

Plná znaková sada se jmenuje `UTF-32`. Každý znak zabírá 4 bajty, jenže většina latinkou psaného textu je už zahrnuta v ASCII, ze kterého historicky spousta dalších znakových sad vycházela.

`UTF-8` je varianta, která toto zohledňuje. Prvních 8 bajtů odpovídá ASCII a ty další 3 bajty lze vynechat. Pokud ale potřebuji vyjádřit znak, který v ASCII není, jako například české "ř" nebo emoji tak se využijí i zbývající 2 až 4 bajty. Díky tomu `UTF-8` šetří místem a zároveň je kompatibilní s jakýmkoliv textem napsaným v ASCII.

## Historické české znakové sady

Každý ajťák by si měl všude vynucovat Unicode. Bez diskuze. Unicode je totiž záruka, že zde lze použít jakýkoliv jazyk a nemusíte už řešit podporu různých znakových sad.

Jediný argument, proč používat jinou znakovou sadu je jen tehdy, pokud musíte pracovat se starým softwarem, který Unicode ještě nezná nebo jste nějakým jiným způsobem donuceni použít něco jiného, než Unicode. Je tedy dobré vědět, že historicky existují tyto české znakové sady, na které můžete narazit:

- ISO-8859-2
- Windows-1250
- Kód Kamenických

## „Rozsypaný čaj“

Upřímně jsem šťastný, že už doba problémů špatných konverzí mezi různými znakovými sadami pominula. Už jen velice vzácně narážím na situace, kdy se mi český text zobrazuje ve špatné znakové sadě, než v jaké byl uložen.

Je ale dobré rozumět tomu, co se děje, když na to narazíte. Jakmile se pokusíte zobrazit nějaký text ve znakové sadě, se kterou daný text nebyl uložen, uvidíte "rozsypaný čaj".

- Žluťoučký kůň úpěl ďábelské ódy (uloženo a zobrazeno `UTF-8`)
- Ĺ˝luĹĄouÄŤkĂ˝ kĹŻĹ ĂşpÄ›l ÄŹĂˇbelskĂ© Ăłdy (`UTF-8` zobrazeno ve `Windows-1250`)
  - možná to nejde úplně poznat ale všimněte si, že písmena bez diakritiky prošla. To právě díky tomu, že `UTF-8` i `Windows-1250` vycházejí z ASCII, kde jsou znaky anglické abecedy, které jsou stejné i v češtině.

[^u]: V případě USB to je [USB HID](https://www.usb.org/sites/default/files/documents/hut1_12v2.pdf), strana 53. Operační systém se stará o to, aby přeložil signál z klávesnice do **aktivní znakové sady**. O tom se budeme bavit ale až v kapitole o operačních systémech.