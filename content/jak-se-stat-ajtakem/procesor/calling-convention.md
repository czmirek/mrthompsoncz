---
draft: false
title: Calling convention
weight: 70335
---

V předchozí kapitole o [podrutinách]({{< relref "ridici-instrukce-2" >}}) jsem uvedl příklad, jak lze dělat podrutiny jen s pomocí `JUMP` instrukce. 

**Je nutné ale zdůraznit, že šlo pouze o příklad.** V moderních procesorech lze stejného výsledku dosáhnout obrovským množstvím jiných způsobů.

V mém příkladu s `JUMP` instrukcí je problém v tom, že to není *skutečná funkce*.   



Z toho důvodu existují **calling conventions** neboli "volací konvence".



Každá instrukční sada obsahuje víc než jednu volacích konvencí. Volací konvence je jinými slovy soubor pravidel které určují:

- jak se mají správně dělat podrutiny
- jak se mají podrutiny správně volat
- jak se dokončené podrutiny mají po ukončení správně vracet do kódu, který rutinu zavolal

<div class="note-blue">

⚠️ **Konvence není závazná.** Programy nemají povinnost konvence dodržovat u svých vlastních podrutin ale mají povinnost konvenci dodržovat pokud chtějí využívat OS API.

</div>

## Nejběžnější volací konvence

- **x86**: `fastcall`, `stdcall`, `cdecl`
- **ARM**: `Procedure Call Standard`


<div class="note-blue">

⚠️ **Běžný ajťák se volacími konvencemi nezabývá**. Běžný ajťák (v mém pojetí) totiž netvoří software na úrovni podrutin a volacích konvencí.

</div>