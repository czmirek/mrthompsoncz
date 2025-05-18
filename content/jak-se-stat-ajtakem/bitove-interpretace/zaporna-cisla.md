---
draft: false
title: Celá záporná čísla
weight: 7050
---

Jak počítače pracují se zápornými čísly?

## Znaménkový bit

Jedna možnost je vzít jeden bit zkraje a říct, že reprezentuje plusovou nebo mínusovou hodnotu. 

Například:
- **42** = <span style="color:red">**1**</span><span style="color:orange">**0101010**</span>  
- <span style="color:red">**1**</span> = znaménko plus (+) symbolizující kladné číslo  
- <span style="color:orange">**0101010**</span> = hodnota 42  

No a záporné číslo **-42** by vypadalo takto.

- **-42** = <span style="color:red">**0**</span><span style="color:orange">**0101010**</span>  
- <span style="color:red">**0**</span> = znaménko minus (-) symbolizující záporné číslo  
- <span style="color:orange">**0101010**</span> = hodnota 42  

## Kladná a záporná nula

Má to však problém: kladnou a zápornou nulu.

0 = 1|0000000 …. +0?  
0 = 0|0000000 …. -0?  

Co se má stát, když sečtete plusovou nulu a negativní nulu? Co když je vynásobíte? Co když vynásobíte kladné číslo zápornou nebo kladnou nulou? 

<div class="note-blue">

Tento způsob se nepoužívá [^p] protože kladná nebo záporná nula nemá reálný základ. Nula je jenom jedna a nemá znaménko.

</div>

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

![Xkcd](https://imgs.xkcd.com/comics/cant_sleep.png)

[^p]: *V kapitole o desetinných číslech zjistíte, že to není zas tak úplně pravda.*