---
draft: false
title: 'Softwarové přerušení'
weight: 70340
---

**Softwarové přerušení** je situace kdy nějaká instrukce, záměrně či nezáměrně, vyvolá přerušení obdobně, jako u [hardwarového přerušení]({{< relref "preruseni" >}}).

- **Záměrné vyvolání přerušení** je mechanismus běžně používaný operačními systémy a ve vývoji softwaru. K tomu se ještě vrátíme později v kapitolách o operačních systémech a tvorbě softwaru.

- **Nezáměrné vyvolání přerušení** může způsobit chybné použití instrukce.

  - Typický příklad je dělení nulou u instrukce pro dělení čísel.
  - Nebo se snažíte zapsat na adresu v paměti, která neexistuje
  - A podobně.

## Vyvolání přerušení

Funguje to velmi podobně, jako hardwarové přerušení.

Místo signálu zvenčí je však signál přerušení vygenerovaný instrukcí přímo v procesoru.

{{< figure align=center width=500 src="../swinterrupt1.png" title="Přerušení - krok 1" >}}

V signálu přerušení je odkaz na funkci/rutinu, která přerušení zpracovává. Změní se tok instrukcí.  

{{< figure align=center width=500 src="../interrupt2.png" title="Přerušení - krok 2" >}}

Jakmile je funkce/rutina zpracovaná a dokončená tak tok instrukcí naváže tam, kde skončil.

{{< figure align=center width=500 src="../interrupt3.png" title="Přerušení - krok 3" >}}
