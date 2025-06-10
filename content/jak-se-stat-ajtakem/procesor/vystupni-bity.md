---
draft: false
title: Výstupní bity
weight: 70060
description: Jak procesor komunikuje výsledky svých instrukcí se zbytkem počítače a proč to není pro běžného ajťáka důležité
---

Výstupní bity jsou instrukce prováděné procesorem na zbytku systému v počítači. **Nemají žádnou pevnou šířku, dokonce ani žádný společný kanál**, kterým by společně putovaly všechny výstupní instrukce, jako je to u vstupních bitů.

<div class="note-blue">

⚠️ **Důležité k zapamatování**: Výstupní bity nejsou důležité. Toto "zadrátování" se liší podle *patice* procesoru což je fyzická zásuvka, do které se na základní desce procesor umisťuje. Tyto specificky detaily jsou pro běžného ajťáka nepodstatné.

</div>

{{< figure align=center width=600 src="../vystup-komplex.png" title="Komplexita výstupních bitů" >}}

Procesor komunikuje se zbytkem počítače prostřednictvím **sběrnic** na základní desce. O těch píšu v pozdější kapitole.