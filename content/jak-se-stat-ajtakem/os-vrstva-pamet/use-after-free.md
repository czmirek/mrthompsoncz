---
draft: false
title: 🩸 Use after free
weight: 218000
---

<div class="note-blue">

**⚠️⚠️⚠️ Extra důležité k zapamatování ⚠️⚠️⚠️**

OS se stará pouze o přidělování a odebírání paměti, běžně se ale **nikdy nestará o obsah**.

Jakmile v paměti nastavíte jakékoliv bity a pak tu paměť dealokujete tak OS na ty bity už znovu nesahá a nechává je, tak jak jsou. OS pak klidně může prostor obsahující tyto bity přidělit **jinému procesu!**

</div>

**Toto má velký vliv na bezpečnost**. V paměti jsou často uložené citlivé údaje, jako například hesla. OS vám zaručuje, že žádný jiný proces nemůže přistoupit k paměti vašeho procesu ale už vám nezaručuje, co se s vaší pamětí stane, jakmile ji dealokujete.

Pokud váš program chybně dealokuje paměť tak tato hesla mohou být odhalena --- této situaci se říká **🩸 use after free** [^1] .

[^1]: *Kapka krve v tomto návodu symbolizuje "zranitelnost" nebo "bezpečnostní problém".*