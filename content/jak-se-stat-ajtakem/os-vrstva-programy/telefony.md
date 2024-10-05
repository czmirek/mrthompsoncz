---
draft: false
title: Procesy v telefonních OS
weight: 201100
---

Menší odbočka k telefonům. Telefonní OS (**Android a iOS**) k procesům přistupují trochu jinak. 

Telefonní OS se snaží šetřit baterii, pracují s méně výkonnými procesory a mají k dispozici menší RAM paměť než jiná zařízení. Z těchto důvodu na svoje procesy dohlíží mnohem pozorněji než je zvykem u "ne-mobilních" OS.

Co se práce s procesy týká tak je chování telefonních OS nepredikovatelné.  

Telefonní OS zpravidla neumožňují uživatelům "tvrdé" zabití procesu, pouze vyslání signálu k ukončení procesu. OS se ale může místo toho rozhodnou proces pouze pozastavit a upozadit --- opětovné rozeběhnutí pozastaveného procesu je totiž mnohem rychlejší než nastartování nového procesu a tedy šetrnější na využitou energii procesoru.

Jindy se telefonní OS může rozhodnout, že aplikaci pošle signál o ukončení ale dá ji nějaký časový limit. Pokud se proces do časového limitu neukončí tak jej OS "zabije". Během tohoto čekání se však může situace změnit (např. se uvolní paměť) a OS své rozhodnutí změní.