---
draft: false
title: Calling convention
weight: 211000
---

**Stack segment** už je trochu složitější struktura a pro její pochopení se musíme vrátit ke kapitole o [podrutinách]({{< relref "../procesor/ridici-instrukce-2" >}}).

{{< figure align=center width=500 src="../../procesor/podrutina.png" title="Podrutina" >}}

V kapitole o podrutinách jsem uvedl příklad, jak lze dělat podrutiny jen s pomocí JUMP instrukce. **Je nutné ale zdůraznit, že šlo pouze o příklad.** V moderních procesorech lze stejného výsledku dosáhnout obrovským množstvím jiných způsobů.

Z toho důvodu existují  **calling conventions** neboli "volací konvence". Každá instrukční sada obsahuje víc než jednu volacích konvencí. Volací konvence je jinými slovy soubor pravidel které určují:

- jak se mají správně dělat podrutiny
- jak se mají podrutiny správně volat
- jak se dokončené podrutiny mají správně vracet do předchozího kódu

<div class="note-blue">

⚠️ **Konvence není závazná.** Programy nemají povinnost konvenci dodržovat u svých vlastních podrutin ale mají povinnost konvenci dodržovat pokud chtějí využívat OS API.

</div>

## Nejběžnější volací konvence

- **x86**: `fastcall`, `stdcall`, `cdecl`
- **ARM**: `Procedure Call Standard`


<div class="note-blue">

⚠️ **Běžný ajťák se volacími konvencemi nezabývá**. Běžný ajťák (v mém pojetí) netvoří software na tak úrovni volacích konvencí.

</div>