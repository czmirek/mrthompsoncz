---
draft: false
title: Hardwarové složitosti které lze ignorovat
weight: 260
---

V kapitole o procesoru jsem pojmenoval Von Neumannovu architekturu, na které jsou všechny moderní počítače postavené

V moderních počítačích je ale realita mnohem komplexnější.

Každá komponenta v počítači běží pod určitou rychlostí, stejně jako procesor. Architektura moderního počítače obsahuje obrovské množství různých „pomocných“ obvodů a čipů, nebo „bufferů“ které slouží právě k dočasnému uložení dat mezi komponentami, které pracují na různých rychlostech.

Samotný procesor obsahuje přímo v sobě sadu různých „miniaturních pamětí“ kterým se říká „cache“ která jsou odstupňované od nejrychlejší (L1) po nejpomalejší (až L4) a tyto „cache“ mohou být v procesoru vyrobeny i za použití jiné výrobní technologie. Data, se kterými procesor „právě tento okamžik“ pracuje se nachází v „registrech“.

Toto dále zesložiťuje fakt, že každý výrobce k tomu může mít jiný přístup.

- Každá základní deska může obsahovat úplně jiné uspořádání čipů/bufferů
- Každá komponenta může obsahovat úplně jiné uspořádání čipů/bufferů
- Každý procesor může obsahovat úplně jiné uspořádání „cache“ a „registrů“

Realita, jak a kudy tečou v moderních počítačích data, by se lépe dala znázornit následujícím obrázkem.

![Hardwarové složitosti které lze ignorovat](/jak-se-stat-ajtakem/fyzicka-vrstva/hwcmp.png)

<div class="note-blue">

Pointa této kapitoly je, že to není pro nás ajťáky vůbec důležité!
Tyto složitosti na úrovni hardwaru nejenom, že často neznáme ale ani je pro svoji práci vůbec znát nepotřebujeme. Důležité je pouze chápat Von Neumannův model.

</div>

---

<div class="note-blue">

Každý hardware funguje uvnitř dost odlišně už jen proto, že výrobci hardwaru si navzájem konkurují výkonem, spolehlivostí a kompatibilitou.

</div>

## Jak ajťáci řeší vadný hardware

Vraťme se v předchozímu příkladu. Řekněme, že si koupíme nový počítač, který zrovna obsahuje čipy, které například pojmenuji X1 a X2. My nevíme, že tam takové čipy jsou ale máme zrovna smůlu, čip X1 je přímo z výroby vadný.

To se může projevit plejádou podivných příčin – počítač se sám od sebe automaticky restartuje, náhodně zamrzává a nelze s ním pracovat, zobrazuje podivné, kryptické chybové hlášky.

Oprava je teoreticky (!) jednoduchá – stačí na základní desce vyměnit čip X1.

Jenže to my nevíme, neumíme to zjistit a ani to neumíme opravit.

My ajťáci téměř nikdy nevíme nic o tom, že na základních deskách tohoto výrobce jsou nějaké čipy X1 a X2 a vlastně v tomto příkladu ani nevíme, jestli je chyba vůbec v základní desce nebo je vada v uložišti. Proto způsob, jakým podobné chyby řešíme, je vylučovací metodou pokus-omyl kdy různě zapojujeme různá zařízení, o kterých víme, že v jiném zapojení zaručeně fungují.

Jakmile identifikujeme, které zařízení je vadné, letí do popelnice (nebo na reklamaci).

## Souhrn

- Zapojení hardwaru je v realitě mnohem komplexnější.
- V každém počítači je tato komplexita hodně odlišná díky konkurenci mezi jednotlivými výrobci hardwaru.
- Nás ajťáky (podle mé definice ajťáka) tato komplexita nezajímá.
- Pokud je něco vadné, uplatňujeme vylučovací metodu pokus-omyl a testujeme, které zařízení v jakém zapojení funguje a které ne.
- Jakmile zjistíme, co je vadné, zbavíme se toho a vyměníme to celé.