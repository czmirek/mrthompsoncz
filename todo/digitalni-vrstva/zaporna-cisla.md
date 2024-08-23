---
draft: true
title: Záporná čísla
weight: 420
---

V tuhle chvíli byste měli mít dobrou představu o tom, jak se v počítačích pracuje s celými čísly. Už víte, že počítače jsou signální přístroje, že každý signál si lze představit jako číslo ve dvojkové soustavě které lze převést do desítkové soustavy.

Takže když řeknu, že číslo 42 je ve dvojkové soustavě 101010 tak už víte, o čem mluvím.

Jak ale v počítači vypadá záporné číslo –42?

## Jak na negativní čísla?

Řekněme, že máme 1 bajt. Už víte, že 1 bajt = 8 bitů a také, že 8 bitů je číslo v rozsahu 28 nebo od 0 do 255. Od nuly se počítá takto.

0 = 00000000  
1 = 00000001  
2 = 00000010  
3 = 00000011  
…  
42 = 00101010  
…  
255 = 11111111  

Ale co když potřebujete negativní čísla?

Musíte vymyslet jiný „kód“ jakým způsobem se převádí bity (signály v počítači) do celého čísla, které umí být jak kladné tak i záporné!

## Znaménkový bit

Jedna možnost je vzít jeden bit zkraje a říct, že reprezentuje plusovou nebo mínusovou hodnotu. Například:

42 = **1|0101010**  
1 = znaménko +  
0101010 = hodnota 42  

No a záporné číslo -42 by vypadalo takto.

-42 = **0|0101010**  
0 = znaménko –  
0101010 = hodnota 42  

To vypadá jako celkem jednoduché, přímočaré řešení, že?

Má to však problém: kladnou a zápornou nulu.

0 = 1|0000000 …. +0?  
0 = 0|0000000 …. -0?  

Co se má stát, když sečtete plusovou nulu a negativní nulu? Co když je vynásobíte? Co když vynásobíte kladné číslo zápornou nebo kladnou nulou? Tento způsob se nepoužívá* protože kladná nebo záporná nula nemá reálný základ. Nula je jenom jedna a nemá znaménko.

\**(v kapitole o desetinných číslech zjistíte, že to není zas tak úplně pravda)*

## Dvojkový doplněk

Pokud máte 8 bitový rozsah, tak začátek vypadá úplně stejně, jako kdybyste počítali mezi dvěma číselnými soustavami.

0 = 00000000  
1 = 00000001  
2 = 00000010  
3 = 00000011  
…  
42 = 00101010  

Ale: jakmile vyplníte všechny bity kromě prvního na 1, uděláte následující.

- Přičtete k číslu +1
- Změníte znaménko na mínus
- Začnete počítat pozpátku

Tzn.

126 = 01111110  
127 = 01111111  
-128 = 10000000  
-127 = 10000001  
-126 = 10000010  
-125 = 10000011  
…  
-1 = 11111111  

## Souhrn

- Procesor pracuje s čísly v určitém rozsahu.
- Pro negativní čísla se může používat znaménkový bit, s ním ale vzniká nesmyslný koncept záporné a kladné nuly, který nemá žádný reálný základ, proto se nepoužívá.
- Pro reprezentaci záporného celého čísla se používá dvojkový doplněk.