---
draft: true
title: Proces a vlákno
weight: 200400
---

Doposud jsem užíval pojem "program" ale tento pojem v operačních systémech má specifický význam.

## Program, aplikace

"Program" potažmo "aplikace" jsou v kontextu OS soubory, které je možné **spustit**. Jinými slovy, jsou to někde uložené **instrukce pro procesor** které samy o sobě nic nedělají. Nejdřív je nutné instruovat OS aby program spustil.

Běžný český uživatel většinou používá OS Windows a v něm běžně spouští program ve Windowsech (většinou dvojitým) poklepáním na nějakou ikonku.

{{< figure align=center src="../wowikona.png" title="Ikonka na ploše v operačním systému Windows" >}}

## Proces

Jakmile se program spustí tak se pro něj vytvoří **proces**. Proces je však pouze něco jako evidenční záznam který shromažďuje důležité informace pro další věci, které se v rámci procesu dějí.

## Entry point

Při vytvoření nového procesu z nějakého programu OS najde jeho **entry point** což je jinými slovy místo, kde pro daný program začínají instrukce, které mohou začít téct pro procesor.

Tento entry point je standard který je **odlišný mezi různými OS**. Z tohoto důvodu není možné aplikaci na Windows spustit např. na macOS a naopak.

## Vlákno
...
