---
draft: false
title: Počet cyklů
weight: 705
---

U moderních procesorů za běžného provozu je prakticky nemožné odhadnout, kolik cyklů jaká instrukce zabere z následujících důvodů.

- **Prediktivní mechanismy**
  - Moderní procesory si ukládají krátkodobou statistiku nejpoužívanějších instrukcí a jejcih výsledků. V některých krocích se tedy snaží odhadnout výsledek, aby mohly hromadu dalších kroků přeskočit a být tak rychlejší.
  - V nějaký moment si však musí ověřit, že skutečný výsledek je totožný s predikcí. Pokud predikce selže, musí se celá mašinérie *CPU pipeline* vrátit o několik kroků zpátky a instrukce se musí provést v jednotlivých krocích řádně, bez použití prediktivních kroků.[^b]

- Některé instrukce mohou některé kroky přeskočit v závislosti na výsledcích instrukcí, které proběhly před nimi.

- Procesor může detekovat, že některé instrukce mohou být přeskočeny a výsledek bude stejný.

- Procesor může v nějakém kroku detekovat, že při příchodu nějaké speciální instrukce může rovnou všechny následující instrukce za ní (až do nějakého momentu) zahodit

⚠️ **Důležité k zapamatování**: Běžný ajťák *většinou* nezná konkrétní instrukce natož aby věděl kolik cyklů která instrukce provede.

[^b]: Běžný uživatel si toho nevšimne. K selhání CPU predikcí dochází ve vašem běžném počítači každou chvíli. Poměr úspěšných predikcí je však v běžném provozu vysoký a proto se výrobcům CPU vyplatí takové prediktivní systémy do CPU zabudovávat.