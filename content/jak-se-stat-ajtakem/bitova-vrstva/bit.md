---
draft: false
title: Bit
weight: 602
---

Číslo 1 nebo 0 se v IT nazývá **bit** (vyslovuje se stejně jako se čte).

<div class="note-blue">

⚠️ Bit je **nejmenší a nedělitelná jednotka informace**. Nic menšího než bit neexistuje.

</div>

{{< figure align=center width=200 src="../twobits.png" title="Bit 0 a 1" >}}

## Práce s bity

Počítače nejsou nic jiného než zařízení, která pracují s **bity** pouze následujícími způsoby:

- **bity jsou uložené**
  - **persistentně** tzn. tyto bity jsou zachované i po vypnutí zařízení
  - **v RAM paměti** tzn. tyto bity jsou ztracené po vypnutí zařízení 
- **bity se od někud někam posílají**
- **bity se proměňují** --- to je velice jednoduché protože jsou možné jen dvě změny:
  - 0 se promění v 1
  - 1 se promění v 0

Každá běžná komponenta **komunikuje se zbytkem systému po binární vrstvě** tedy prostřednictvím bitů.

## Slovník k zapamatování

- **bit**: hodnota 0 nebo 1
- **X bitů**: toto může znamenat 2 věci, záleží na kontextu
  - šířka možných hodnot
    - 5 bitový = rozsah, ptáme se *"Kolik jedniček a nul vedle sebe můžeme dát?"*
  - číselná hodnota s konkrétní šířkou
    - 5 bitů = hodnota, číslo mezi 00000 a 11111, ptáme se *"Jaká je to hodnota?"*
    - O číslech si povíme později v kapitole o dvojkové soustavě.

**Pamatuj:**

- Počet bitů přídavným jménem - 5 bitový - znamená označení šířky možných hodnot.
- Počet bitů podstatným jménem - 5 bitů - znamená hodnotu. 

## Vše ostatní je práce s bity

Vše co budete číst po této kapitole je už práce s bity. Běžný ajťák **musí** dobře rozumět počítačům právě od bitové vrstvy. K tomu máte naštěstí tento návod.