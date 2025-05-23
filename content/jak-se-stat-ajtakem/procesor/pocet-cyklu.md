---
draft: true
title: Počet cyklů
weight: 79950
---

U moderních procesorů za běžného provozu je prakticky nemožné odhadnout, kolik cyklů jaká instrukce zabere z následujících důvodů.

- **Prediktivní mechanismy**
  - Moderní procesory si ukládají krátkodobou statistiku nejpoužívanějších instrukcí a jejich výsledků. V některých krocích se tedy snaží odhadnout výsledek, aby mohly hromadu dalších kroků přeskočit a být tak rychlejší.
  - V nějaký moment si však musí ověřit, že skutečný výsledek je totožný s predikcí. Pokud predikce selže, musí se celá mašinérie *CPU pipeline* vrátit o několik kroků zpátky a instrukce se musí provést v jednotlivých krocích řádně, bez použití prediktivních kroků. [^b]

- **Optimalizace instrukcí**
  - Některé instrukce mohou některé kroky přeskočit v závislosti na výsledcích instrukcí, které proběhly před nimi.
  - Procesor může detekovat, že některé instrukce mohou být přeskočeny a výsledek bude stejný.
  - Procesor může v nějakém kroku detekovat, že při příchodu nějaké speciální instrukce může rovnou všechny následující instrukce za ní (až do nějakého momentu) zahodit
  - Atd. apod.

⚠️ **Důležité k zapamatování**: Běžný ajťák *většinou* nezná konkrétní instrukce natož aby věděl kolik cyklů která instrukce provede.

## Determinismus a nedeterminismus

- **Deterministické** znamená, že za stejných podmínek se něco chová pořád stejně. 
- **Nedeterministické** tedy znamená,že **za stejných podmínek se vždy chová jinak**.

---

Pro procesor platí, že:

- **Vykonání instrukcí je vždy deterministické**. Instrukce, které pošleme do procesoru, vždy vyplodí stejný výsledek. Pokud by toto neplatilo, nemohly by procesory fungovat.

- **Vnitřní chování procesoru je nedeterministické**. To znamená, že při každém spuštění těch samých instrukcí se procesor může pokaždé rozhodnout pro jiný způsob řešení.

--- 

**Příklad:** 

Řekněme, že máte přesně daný seznam instrukcí. Tyto instrukce reprezentují nějakou aplikaci, která vypočte nějakou matematickou úlohu. Tato vaše aplikace je **deterministická** to znamená, že daný seznam instrukcí vždy vede ke stejnému výsledku.

Máte zároveň k dispozici laboratoř ve které zkoumáte, jak jednotlivé instrukce této aplikace putují nějakým moderním procesorem.

Pokaždé, když instrukce do procesoru pustíte tak se matematická úloha vypočte vždy stejně. Vaše aplikace je deterministická takže je to očekávatelné chování.

Když se ale ve své laboratoři pomocí nějakých přístrojů podíváte na **putování instrukcí v procesorové pipelině** tak při každém spuštění můžete vidět nějaký drobný rozdíl. To znamená, že chování moderních procesorů je **nedeterministické**

[^b]: *Běžný uživatel si toho nevšimne. K selhání CPU predikcí dochází ve vašem běžném počítači každou chvíli. Poměr úspěšných predikcí je však v běžném provozu vysoký a proto se výrobcům CPU vyplatí takové prediktivní systémy do CPU zabudovávat.*