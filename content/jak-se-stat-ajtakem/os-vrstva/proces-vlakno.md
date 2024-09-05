---
draft: false
title: Virtuální paměť
weight: 906
---

Určitě jste sami několikrát zažili postup instalace nějaké aplikace/programu. Nejdřív stáhnete nějaký soubor, ten pak spustíte, něco se nainstaluje a vy pak ten program spustíte.

Instalátory jsou samy o sobě nějaké programy. Aplikace, která neběží, je pouze seznam instrukcí v nějakém úložišti jako třeba HDD/SDD.

Jakmile spustíte nějakou aplikaci tak OS udělá několik věcí:

- OS vytvoří nový proces
- V dané aplikaci se najde entry point a přidělí se mu hlavní vlákno pod kterým se proces rozeběhne

## Proces

Proces je prostě jenom pojmenování pro běžící aplikaci. To je fakt úplně všechno. Každý proces může spustit podproces ale Windowsy a Linuxy s podprcesy pracují odlišně.

- Linux: jakmile hlavní proces skončí tak podprocesy skončí s ním
- Windows: podprocesy běží i po skončení hlavního procesu

Proces ale není to co běží, proces je jenom způsob seskupování běžících aplikací a jejich vláken. To co „běží“ je ve skutečnosti hlavní vlákno. Viz. níže.
Entry point

Každá aplikace obsahuje entry point, což je místo, kde začínají instrukce tohoto programu. Hlavní vlákno procesu začíná spouštět instrukce v entry pointu.

## Vlákno (thread)

Vlákno nebo anglicky „thread“ je něco jako „běžící jednotka“ nebo „přidělený procesor“ nebo přidělená kapacita spouštět instrukce. Vlákno se spustí a spouští instrukce které jsou k tomuto vláknu přidělené. Po provedení všech instrukcí vlákno skončí.

Vlákno bez instrukcí se po nastartování ihned ukončí. Seznam vláken si operační systém spravuje v paměti (v kernel space).

U vlákna se tedy rozlišuje jeho stav který může být:

- Běžící (running)
- Ukončený (terminated/killed/stopped atd.)

Toto jsou dva základní stavy, které jsou společné pro Windowsy i Linuxy. Oba operační systémy podporují i nějaké další stavy jako např. „pozastavené“, „přerušitelné“, „nepřerušitelné“, to už je ale v rámci této kapitoly nepodstatný detail.
Hlavní vlákno

Hlavní vlákno je vlákno, které z pohledu OS reprezentuje běžící program. Proces je pouze kategorizace, „aplikace/program“ to je jen názvosloví, jak tomu říkají lidé. Co ale skutečně v aplikaci běží je jeho hlavní vlákno.

Běžící aplikace = běžící hlavní vlákno aplikace.

Proč ale „hlavní“?

Protože jakákoliv aplikace – respektive jakékoliv vlákno – si může říct operačnímu systému o vytvoření dalšího vlákna.

Ale pozor: jakmile hlavní vlákno skončí, skončí i všechna ostatní vlákna a celý proces! Toto je stejné pro Windows i pro Linuxy.

![Proces a vlákno](/jak-se-stat-ajtakem/os-vrstva/proces.png)

Pozor na to, nepleťte si vlákna a procesy. Proces je jen obal okolo hlavního vlákna, potažmo dalších vláken, které v rámci procesu běží. Při skončení hlavního vlákna jsou ukončena i všechna ostatní vlákna, která v procesu patří.

OS normálně nedovoluje procesům, aby jejich vlákna četla data z vláken jiných procesů nebo vlákna jiných procesů ovlivňovala. V rámci jednoho procesu je to ale možné. Každá aplikace má totiž od OS přidělený svůj kus v paměti a co si každá aplikace ve svém kusu paměti dělá a kolik vláken ji tam běží, to je její odpovědnost.

Možná se teď ptáte:

- Proč aplikace potřebuje víc vláken?
- Jak je vůbec možné, že aplikace běží s více než jedním vláknem? Procesor přeci zpracovává instrukce za sebou. Nemůže zpracovávat instrukce paralelně, ne?
- A jak je vůbec možné, že v rámci OS může běžet víc aplikací? Tedy víc jak jedno vlákno?

O tom si povíme v příštím díle.

<div class="note1">

Zajímavost: „Fork bomb“ je název pro záškodnickou aplikaci, která obsahuje jen tuto instrukci: Instrukce A: vytvoř vlákno, jehož obsahem je instrukce A. „Fork bomb“ tedy vytváří vlákna donekonečna, dokud OS nedojde paměť nebo výpočetní kapacita procesoru a počítač se úplně odstaví. („fork“ je název Linuxové funkce pro vytvoření nového procesu)

</div>

## Shrnutí

- OS při spuštění aplikace vytváří proces. Proces je pouze kategorizace a pojmenovávání běžících aplikací.
- Aplikaci je přiděleno hlavní vlákno na entry pointem.
- Entry point je místo, kde začínají instrukce aplikace.
- Vlákno je základní běžící jednotka.
- Jakékoliv vlákno může zažádat OS o vytvoření dalšího vlákna se zadanými instrukcemi.
- Vlákno může být ve 2 základních stavech: běžící a ukončené. Windows a Linuxy podporují u vláken další různé stavy s různými pravidly, jak se z jednoho stavu lze dostat do jiného.
- Skončení hlavního vlákna znamená konec celého procesu a všech jeho vláken.