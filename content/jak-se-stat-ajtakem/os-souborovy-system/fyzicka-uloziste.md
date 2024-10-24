---
draft: false
title: Fyzická uložiště
weight: 301000
---

V IT provozech se běžný ajťák setká většinou jen s SSD, HDD a USB flash pamětí. Na HDD jsou data uložena na zmagnetizovaných plotnách ve formě miniaturních rozdílů v magnetické polaritě, v SSD jsou data uložena formou zachovaného elektrického náboje.

Každé fyzické uložiště si lze představit jako obrovský rozsah bitů, který má začátek a nějaký konec. Každý bit je na nějaké **pozici**.

{{< figure align=center width=600 src="../disksimple.png" title="Bity v disku" >}}

Disky jsou fyzicky rozdělené na **sektory** které však mají různé velikosti. U HDD to bývá 512 bajtů, u SSD 4 kilobajty (4096 bajtů), velikosti sektorů se však mohou mezi výrobci lišit. 

Tyto sektory jsou nejměnší **adresovatelné** celky, ze kterých fyzicky lze bajty číst a do kterých lze zapisovat.

To znamená, že: 
- pokud chcete přečíst jen jeden bajt, **musíte stejně přečíst celý sektor**.
- pokud chcete změnit jen jeden bajt, **musíte stejně zapsat na celý sektor**.

{{< figure align=center width=400 src="../sektory.png" title="Sektory" >}}