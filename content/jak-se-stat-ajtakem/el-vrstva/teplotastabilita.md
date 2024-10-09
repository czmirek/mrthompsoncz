---
draft: false
title: Teplota a chlazení
weight: 304
---

Každý obvod, například i měděný kabel od zásuvky zasekaný do zdi, má nějaký přirozený elektrický odpor a jakmile skrz něj putuje elektřina tak díky tomuto odporu se generuje teplo. Pokud byste měli ve zdi kabel který zvládne maximálně 10 ampérů připojený na 16 ampérový jistič, můžete regulérně vyhořet.

Čipy v běžných počítačích - včetně procesoru nebo grafického čipu - jsou vyrobeny z miniaturních obvodů které se měří na nanometry. Jeden nanometr je 0.0000001 milimetru. Těchto obvodů je v čipech obrovské množství naskládaných na sobě v mnoha vrstvách. 

V takovém množství se začne sčítat teplo generované jednotlivými obvody. A to takovým způsobem, že to může být problém - citlivé, miniaturní obvody se mohou začít poškozovat a rozpadat **a to mnohem dřív, než se z procesoru viditelně začne kouřit**. 

Jediný zničený obvod z miliardy obvodů prakticky znamená celý zničený procesor; u čipů/procesorů neexistuje žádná možnost opravy.

## Chlazení

Některé čipy za **běžného provozu** produkují teplo ale mohou fungovat i bez dalšího chlazení.

Výkonější čipy vyžadují aspoň **pasivní chlazení** což jsou takové žebrovité struktury přilepené přímo na čip. Tyto struktury jsou vyrobené z materiálu, který velmi dobře odvádí teplo.

{{< figure align=center width=200 src="../passivecooling.png" title="Pasivní chlazení" >}}

Nejvýkonější čipy - zpravidla na procesorech a na lepších grafických kartách - vyžadují **aktivní chlazení** ve formě větráku nebo vodního chlazení.

{{< figure align=center width=100 src="../aktivnichlazeni.png" title="Aktivní chlazení" >}}

## Chlazení procesorů v běžných PC

Procesory v běžných moderních počítačích jsou vybavené teplotními čidly a pokud neděláte nějaké neobvyklé věci (jako např. overclocking, viz. níže) tak se vám nestane, že byste procesor omylem zníčili. Díky teplotním čídlům si procesor aktivní chlazení reguluje sám. 

Pokud větráček odstraníte, moderní procesor bude fungovat i bez chlazení avšak za cenu obrovského snížení výkonu (tudíž i vyprodukovaného tepla). Toto obrovské snížení výkonu je u moderních procesorů brutální, až nad 90% a jakákoliv normální práce s počítačem je prakticky nemožná.

## Overclocking

Overclocking je praxe, kdy se z procesorů "vymačkává" další výkon. Do procesoru se jednoduše posílá vyšší napětí, procesor se pak víc přehřívá a kvalitní chlazení je nutnost.

Overclocking však **není** normální praxe pro běžné ajťáky ale spíš pro hráče her a různé hračičky, proto se na něj víc soustředit nebudu.