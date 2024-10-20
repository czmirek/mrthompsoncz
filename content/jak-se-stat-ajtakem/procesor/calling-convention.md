---
draft: false
title: Calling convention
weight: 70335
---

V předchozích kapitolách o [podrutinách]({{< relref "ridici-instrukce-2" >}}) a o [funkcích]({{< relref "funkce" >}}) jsem uvedl příklady, jak lze dělat podrutiny nebo funkce se vstupními/výstupními parametry jen s pomocí `JUMP` instrukce. 

**Je nutné ale zdůraznit, že šlo pouze o ukázkové příklady.** V moderních procesorech lze stejného výsledku dosáhnout obrovským množstvím jiných způsobů. Z tohoto důvodu existují **calling conventions** neboli **volací konvence**.

Každá instrukční sada obsahuje víc než jednu volacích konvencí. Volací konvence je jinými slovy soubor pravidel které určují:

- jak se mají správně dělat funkce/podrutiny
- jak se mají funkce/podrutiny správně volat
- jak se mají **správně předávat vstupní parametry**
- jak se má **správně předávat výstupní parametry**
- jak se dokončené funkce/podrutiny mají po ukončení **správně vracet do kódu, který rutinu zavolal**

<div class="note-blue">

⚠️ **Konvence není závazná.** Programy nemají povinnost konvence dodržovat u svých vlastních podrutin ale mají povinnost konvenci dodržovat pokud chtějí využívat OS API.

</div>

## Nejběžnější volací konvence

- **x86**: `fastcall`, `stdcall`, `cdecl`
- **ARM**: `Procedure Call Standard`

<div class="note-blue">

⚠️ Přestože to pro moderní procesory není problém, běžné volací konvence umí pracovat pouze s **jedním výstupním parametrem**. Toto má historické ale i logické důvody, ke kterým se vrátím v kapitolách o programování.

⚠️ **Běžný ajťák se volacími konvencemi nezabývá**. Běžný ajťák (v mém pojetí) totiž netvoří software na úrovni podrutin a volacích konvencí.

</div>