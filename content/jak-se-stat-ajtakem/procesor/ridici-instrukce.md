---
draft: false
title: Řídící instrukce
weight: 732
---

Řídící instrukce je schopna **změnit tok instrukcí**.

Nejznámější a nejpoužívanější řídící instrukcí je instrukce zvaná **JUMP** která přeskočí na tok instrukcí určený adresou této instrukce.

Podívejte se na obrázek níže. Odhadnete, kdy program spuštěný na obrázku níže skončí?

{{< figure align=center width=500 src="../tok-instrukci.png" title="JUMP instrukce" >}}

**Odpověď:** Tento program sám od sebe neskončí a **točí se v nekonečné smyčce**. Procesor čte instrukce v tomto pořadí:

```
- Instrukce A
- Instrukce B
- Instrukce C
- JUMP 2
- Instrukce B
- Instrukce C
- JUMP 2
- Instrukce B
- Instrukce C
- JUMP 2
- ...
```

**POZOR!**: Parametrem **JUMP** je adresa v paměti. JUMP tak může skočit v RAM paměti úplně kamkoliv - dopředu i dozadu ale klidně i do úplně jiného seznamu instrukcí, který se v RAM paměti může také nacházet (pokud jsme si ho tam připravili)!