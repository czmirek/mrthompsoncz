---
draft: false
title: Calling convention
weight: 70335
---

V předchozích kapitolách o [podrutinách / funkcích]({{< relref "fce-podrutina2" >}}) jsem uvedl příklady, jak lze dělat podrutiny nebo funkce se vstupními/výstupními parametry jen s pomocí `JUMP` instrukce. 

**Je nutné ale zdůraznit, že šlo pouze o ukázkové příklady.** V moderních procesorech lze stejného výsledku dosáhnout obrovským množstvím jiných způsobů. 

Z tohoto důvodu existují **calling conventions** neboli **volací konvence**.

## 📜 Co je volací konvence?

Volací konvence je soubor pravidel které určují, jaké instrukce se mají používat a jakým způsobem pro:

- **tvorbu funkcí**: včetně vstupních parametrů a výstupu funkce, pokud ji funkce definuje
- **volání funkcí**: včetně předávání vstupních hodnot a vrácení výstupní hodnoty
  - **vstup do funkce**: jakým způsobem se při volání funkce přejde z jedné podrutiny do další
  - **výstup z funkce**: jakým způsobem se při dokončení konkrétní funkce kód vrátí do podrutiny, která funkci zavolala

<div class="note-blue">

⚠️ **Konvence není závazná.** Programy běžící přímo na procesorech si klidně mohou vymyslet své vlastní konvence. Programy běžící v rámci operačních systémů už nějaké konvence dodržovat musí, protože to od nich operační systémy vyžadují.
 
</div>

## Nejběžnější volací konvence

- **x86**: `fastcall`, `stdcall`, `cdecl`
- **ARM**: `Procedure Call Standard`

<div class="note-blue">

⚠️ **Běžný ajťák se volacími konvencemi nezabývá** (měl by však vědět, že existují). Běžný ajťák (v mém pojetí) netvoří software na úrovni podrutin a volacích konvencí.

</div>