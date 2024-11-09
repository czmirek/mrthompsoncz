---
draft: false
title: Otevření souboru
weight: 305000
---

Žádný proces nemůže do žádného souboru zapisovat nebo z něj číst **pokud ten soubor nejdřív neotevře**. Procesy by po provedení čtení/zápisu měly soubor **zavřít**.

{{< figure align=center width=700 src="../soubor-bezna-manipulace.png" title="Běžný postup práce se souborem" >}}

Definice funkcí v OS API pro práci se soubory totiž vždy vypadají takto:

- `file_descriptor = OTEVŘI_SOUBOR(cesta)`
- `ZAPIŠ_DO_SOUBORU(file_descriptor, start_pozice, bajty)`
- `bajty = ČTI_ZE_SOUBORU(file_descriptor, start_pozice, počet_bajtů)`
- `ZAVŘI_SOUBOR(file_descriptor)`

Všimněte si, že funkce pro zápis a čtení vyžadují nějaký `file_descriptor` [^f] který lze získat pouze zavoláním funkce pro otevření souboru. Tento `file_descriptor` je jen nějaký identifikátor [^i], jakási "karta" díky které OS sleduje, se kterými soubory se zrovna pracuje.

<div class="note-blue">

⚠️ **Důležité k zapamatování**: Pokud proces neuzavře otevřený soubor pak jej za něj uzavře OS v případě, že proces skončí bez uzavření souboru. Pokud však proces nad souborem prováděl nějaké změny tak OS nezaručuje, že se tyto změny v souboru projeví.

</div>


[^f]: *V Linuxu se označuje jako [file descriptor](https://man7.org/linux/man-pages/man2/open.2.html), ve Windows jako [file handle](https://learn.microsoft.com/en-us/windows/win32/api/winbase/nf-winbase-openfile)*
[^i]: *Zpravidla ve formě obyčejného [integeru]({{< relref "../bitove-interpretace/celociselne-rozsahy" >}})*