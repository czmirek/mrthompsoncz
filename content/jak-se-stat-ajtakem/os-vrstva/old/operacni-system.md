---
draft: true
title: Operační systém
weight: 2010
---

Teď už toho víte o počítačích docela dost. Jak počítače pracují s bity a bajty, jak pracují s čísly, zápornými i desetinnými a jak reprezentují znaky.

Z prvních kapitol už máte zároveň nějakou představu o tom, jakou roli v počítači hraje procesor a ostatní komponenty.

## Bare-metal programming

Pokud počítač nemá operační systém tak je to jen kus železa. Procesor čeká na instrukce a pokud žádné instrukce nenajde tak pošle celou vaši rodinu do koncentráku.

Ale víte co, ty instrukce mu můžete dodat napřímo. V historii operační systémy neexistovaly a software se psal tak, že zařízení spustilo program, který jste mu zadali. Jakmile program skončil, počítač se musel ručně vypnout, restartovat (třeba s jiným programem nebo jinými vstupy) nebo se vypnul sám.

Takto můžete programovat počítače i dnes. Říká se tomu bare-metal programming v překladu doslova „programování nad holým železem“.

K tomu se pojí i pojem embedded programming které znamená „programování nad vestavěnými zařízeními“ což se vztahuje na různé drobné počítače vestavěné do nějakého zařízení s konkrétním účelem, například bankomaty.

Existují taková mrňavá zařízení jako například raspberri pi nebo Arduino. Toto jsou prostě jenom miniaturní počítače s ARM procesory. Existuje celá komunita ajťáků, kteří se tomu věnují a pokud se vám líbí myšlenka přímého programování nad zařízením tak nejdřív dočtěte tento návod a pak se zkuste podívat na návod jak napsat operační systém pro raspberry pi.

![RPI](/jak-se-stat-ajtakem/os-vrstva/rpi.jpg)

Varování: bare-metal programming nad běžným stolním PC je sebevražda. Současné operační systémy existují už desítky let, pracovalo na nich za tu dobu tisíce lidí a umí pojmout obrovskou hromadu hardwarových složitostí, které čas od času nějaký nadšenec do technologií chce všechny naprogramovat za víkend. Byli jste varováni.

## Hotový operační systém

Já jsem líný ajťák. Používám odjakživa Windows jak k osobním tak pracovním věcem. Moje práce zahrnuje manipulaci i s nějakým Linuxem. Na telefonu mám Android, což je ve skutečnosti Linux.

Na macOS jsem v životě sáhnul jen párkrát ale nikdy mě Apple produkty nezajímaly a nikdy jsem žádný Apple nevlastnil.

Většina dobře placeného ajťačení, kterému se ajťáci věnují, je na úrovni existujícího operačního systému. Bare-metal programming a psaní operačních systémů se věnují jenom nadšenci, lidé co to mají jako koníček nebo studenti co se chtějí něco naučit….a nebo lidé, kteří reálně pracují na operačních systémech jako Windows nebo Linux, které všichni používáme.

Proto v tomto návodu cokoliv, o čem budu dále mluvit, je ve vrstvě operačního systému. A k tomu je důležité operačním systémům porozumět.


![OS vrstva](/jak-se-stat-ajtakem/os-vrstva/os-vrstva.png)


## Shrnutí

- Bare-metal programming je praxe psaní softwaru přímo pro fyzické zařízení.
- Zkusit si napsat vlastní OS pro raspberri pi může být zábava hraničící s patologickým masochismem.
- Psát vlastní OS pro klasické stolní počítače je zaručeně už jen patologický masochismus bez zábavy.
- Většina ajťačení o kterém budu v tomto manuálu mluvit probíhá na existujícím hotovém operačním systému jako Windows, Linux nebo macOS.