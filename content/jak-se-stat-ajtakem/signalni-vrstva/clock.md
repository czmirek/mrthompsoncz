---
draft: false
title: Časování
weight: 402
---

Řekněme pro jednoduchost, že komponenty spolu komunikují morseovkou[^m]. Elektronická komponenta 1 (EL1) chce odeslat elektronické komponentě 2 (EL2) pozdrav "AHOJ" který je v morseovce `.- .... ---. ---`

EL1 začne vysílat první písmeno "A" tedy `.-`


{{< figure align=center width=500 src="../a.png" title="Co odešle EL1" >}}

Jenže EL2 nevidí písmeno "A" ale písmeno "E".

{{< figure align=center width=500 src="../e.png" title="Co vidí EL2" >}}

Jak je to možné?

## Vnitřní hodiny

EL1 má totiž odlišné vnitřní hodiny od EL2. Pro EL1 je délku signálu 30 mikrosekund ale pro EL2 je délka signálu 50 mikrosekund.

Díky tomu EL2 přečte jenom jeden krátký signál --- což je písmeno "E".

Proč tomu tak je?

Reálně totiž nedává smysl, aby všechny komponenty všude na světě komunikovaly stejně rychle. Některé komponenty mají extrémně rychlé vnitřní hodiny (jako např. procesor), jiné mají pomalejší vnitřní hodiny a neexistuje žádný standard který by říkal, jak rychle má která komponenta fungovat.

## Společný časovač

Řešením tohoto problému je společný časovač, který dvěma a více různým komponentám sděluje délku signálu, na které budou fungovat. 

[^m]: V počítačích se morseovka nepoužívá. Morseovku zde zmiňuji pro jednodušší vysvětlení konceptů v signální vrstvy.