---
draft: false
title: Teplota a chlazení
weight: 304
description: Jak obvody v počítačích generují teplo, proč je důležité je chladit a co to znamená pro běžného ajťáka
---

Každý obvod, například i měděný kabel od zásuvky zasekaný do zdi, má nějaký přirozený elektrický odpor a putující elektřina v něm generuje teplo.

Pokud byste měli ve zdi kabel na max. 10 ampérů připojený na 16 ampérový jistič, můžete regulérně vyhořet.

Čipy v běžných počítačích - včetně procesoru nebo grafického čipu - obsahují miniaturní, nanometr široké obvody. Jeden nanometr je 0.0000001 milimetru. Takových obvodů je v čipech obrovské množství naskládaných na sobě v mnoha vrstvách. 

V takovém množství se začne sčítat teplo generované jednotlivými obvody. To může být problém - citlivé, miniaturní obvody se mohou začít poškozovat a rozpadat **a to mnohem dřív, než se z procesoru viditelně začne kouřit**. 

Jediný zničený obvod z miliardy obvodů prakticky znamená celý zničený procesor. U čipů/procesorů neexistuje žádná možnost opravy.

## Chlazení

Čipy za běžného provozu produkují teplo. Většina čipů nepotřebuje chlazení a teplo jednoduše vyzáří.

Výkonější čipy vyžadují **pasivní chlazení**. To poznáte podle žebrovitých strukturu připevněných k čipu. Pasivní chlazení je vyrobené z materiálu, který velmi dobře odvádí teplo.

{{< figure align=center width=200 src="../passivecooling.png" title="Pasivní chlazení" >}}

Nejvýkonější čipy - zpravidla procesory a grafické karty - vyžadují **aktivní chlazení** ve formě větráku nebo vodního chlazení.

{{< figure align=center width=100 src="../aktivnichlazeni.png" title="Aktivní chlazení" >}}

## Chlazení procesorů v běžných PC

Procesory v běžných moderních počítačích jsou vybavené teplotními čidly a pokud neděláte nějaké neobvyklé věci (jako např. overclocking, viz. níže) tak se nestane, že byste procesor zníčili. Procesor si aktivní chlazení reguluje sám. 

Pokud větráček odstraníte, moderní procesor bude fungovat i bez chlazení avšak za cenu obrovského snížení výkonu (tedy i vyprodukovaného tepla). Snížení výkonu u moderních procesorů je okolo 90% celkového výkonu a jakákoliv normální práce s počítačem je prakticky nemožná.

## Overclocking

Overclocking je praxe, kdy se z procesorů [vymačkává](https://www.youtube.com/watch?v=qr26jxPIDm0) další výkon. Uměle se navyžuje napětí, procesor se víc přehřívá a kvalitní chlazení je nutnost.

Overclocking není praxe běžných ajťáků ale zábava pro hráče her a různé hračičky. V tomto návodu se jím nebudu zabývat.