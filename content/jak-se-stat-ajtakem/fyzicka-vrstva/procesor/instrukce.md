---
draft: false
title: Instrukce procesoru
weight: 251
---

Procesor je hodně zjednodušeně elektronický čip, které umí přijmout nějakou kombinaci signálů na vstupu a na základě této kombinace vyprodukovat jinou kombinaci signálů na výstupu.

![Instrukce procesoru](/jak-se-stat-ajtakem/fyzicka-vrstva/procesor/instrukce.png)

Moderní procesory jsou extrémně komplexní ale v základu je to pořád tento model. Procesor skrz vstupní signály získává instrukce na základě kterých sám něco provádí nebo skrz základní desku přikazuje něco zařízením okolo sebe.

- Skrz základní desku dostává informace od klávesnice a myši
- Skrz grafický čip/kartu posílá informace do obrazovky
- Skrz síťovou kartu komunikuje s internetem
- Skrz RAM pamět si ukládá a znovu načítá nějaké rychle dostupné informace
- Skrz základní desku zadává instrukce pro práci s daty na HDD/SSD disky

Procesor si sám nic nevymýšlí a pouze se řídí instrukcemi. Když zapnete počítač tak první co se v počítači děje je, že procesor společně se základní deskou hledá instrukce.

Pokud žádné nenajde tak s počítačem prakticky nic neuděláte a zobrazí se vám nějaká hláška, která vypadá například takto.

![Boot](/jak-se-stat-ajtakem/fyzicka-vrstva/procesor/boot.png)

S prvními historickými počítači se pracovalo tak, že někdo ručně tahal za páky nebo mačkal tlačítka, které udávaly kombinaci signálů, které znamenaly nějakou konkrétní instrukci. Později se tyto instrukce zadávaly skrz děrkované štítky. Tyto počítače byly schopné rozpoznat konkrétní instrukci podle předepsané struktury děr.


![Děrkované štítky](/jak-se-stat-ajtakem/fyzicka-vrstva/procesor/derkovane.png)

Tyto počítače se používaly prakticky jen pro vědecké/vojenské účely protože jediné co uměly bylo spočítat něco rychleji (například trajektorii rakety) než kdyby to počítal člověk.

Počítače na děrkovací štítky uměly zpracovat 10 až 100 instrukcí za vteřinu. Moderní procesor je schopný zpracovat až 5 miliard (5000000000) instrukcí za vteřinu (toto je prakticky totéž jako údaj, který se udává v procesorech jako „GHz“ například „3,5 GHz“ = 3 a půl miliard instrukcí za vteřinu).

Už nedává žádný smysl psát instrukce pro procesor napřímo. 5 miliard instrukcí za vteřinu je totiž fakt hrozně moc a tak nad instrukcemi pro procesor vzniklo spousta dalších vrstev, nové pohledy a vrstvy, které nám umožňují abstrahovat (viz. předchozí díl) obrovskou složitost a rychlost moderních procesorů. 

### Procesor nemůže nic nedělat

Jsme v životě zvyklí na to, že máme nějaký nástroje na elektřinu, třeba vysavač. Ten zapojíme do elektřiny, pustíme a jak je v provozu tak jej nějak začneme používat.

<iframe width="960" height="540" src="https://www.youtube.com/embed/lybw5fK8TOI" title="急に全てが嫌になったウーパールーパー3" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

Procesor je ale zařízení, které používáme už jen tím, že do něj pouštíme elektřinu. Jakmile je procesor „pod proudem“ tak to znamená, že přijímá instrukce. Protože ten proud, co do procesoru teče, to už jsou konkrétní instrukce!

Procesor nemá žádné „napájení“ protože elektřina, která vstupuje a vystupuje z procesoru už reprezentuje konkrétní instrukční signály.

Procesor, který nedostává instrukce, není pod proudem. Je vypnutý a když je mrtvý procesor tak je mrtvý celý počítač protože procesor říká všem ostatním komponentám, co mají dělat.

Co se děje, když zapnete počítač a vy na něm neděláte? Jaké instrukce pak tečou do procesoru?

Moderní procesory mají pro tento účel „HALT“ instrukci která způsobí, že procesor nic na výstupu nepředá a na velice krátký časový úsek se pozastaví. K této otázce se ještě vrátíme v kapitole o operačních systémech.

## Shrnutí

- Procesor je zařízení, které skrz kombinace vstupních signálů dostává instrukce
- Na základě těchto instrukcí skrz kombinace výstupních signálů něco instruuje na okolní komponenty v počítači
- Procesor nemůže nic nedělat. Jakmile je pod proudem, dostává instrukce. Jakmile není pod proudem, nedostává instrukce.
- Jedna z instrukcí procesoru je „HALT“ při které se procesor pozastaví na krátký časový úsek.