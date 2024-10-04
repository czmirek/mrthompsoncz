---
draft: false
title: Procesy v telefonních OS
weight: 201100
---

Telefonní OS (**Android a iOS**) k procesům přistupují trochu jinak. Telefonní OS se snaží šetřit baterii a zároveň pracují s méně výkonnými procesory a mají většinou k dispozici menší RAM paměť než běžné stolní PC.

Z těchto důvodu telefonní OS na svoje procesy dohlíží mnohem pozorněji, než je zvykem u "ne-mobilních" OS.   

Dále to znamená, že chování telefonních OS je celkem nepredikovatelné, co se práce s procesy týká.  

Telefonní OS zpravidla neumožňují "tvrdé" zabití procesu, pouze vyslání signálu k ukončení procesu. Telefonní OS (oproti běžnému OS) se ale může místo toho rozhodnou proces pouze pozastavit a upozadit --- opětovné rozeběhnutí pozastaveného procesu je totiž mnohem rychlejší než nastartování nového procesu a tedy šetrnější na využitou energii procesoru.

Jindy se telefonní OS může rozhodnout, že aplikaci pošle signál o ukončení ale dá ji nějaký časový limit. Pokud se proces do časového limitu neukončí tak jej OS ukončí násilím. Během tohoto čekání se však může situace změnit (např. se uvolní paměť) a OS svoje rozhodnutí změní.