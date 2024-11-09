---
draft: false
title: Partitioning
weight: 308000
---

Partitioning je bitový standard nebo schéma, kterým se **fyzický disk** člení na *logické disky* neboli **partitions**, často se tomu říká počeštěně "*pártyšny*".

{{< figure align=center width=700 src="../partitions.png" title="Partitions" >}}

Každá partitiona pak obsahuje **svůj vlastní souborový systém**. Tyto souborové systémy dokonce nemusí být stejného typu - každá partitiona může obsahovat jiný FS.

{{< figure align=center width=700 src="../partitions-fs.png" title="Souborové systémy v partitionách" >}}

## Partition standardy

Nejznámější jsou tyto standardy:

- **Master boot record (MBR)**
- **GUID Partition Table (GPT)** - moderní nejpoužívanější způsob

Běžný ajťák však pro partitionování používá pro to určené specializované programy a většinou neřeší, který konkrétní standard se pro partitionování používá.

## Běžné použití partition a FS

Souborový systém lze aplikovat na disk **napřímo** tzn. pro využití souborového systému nemusíte partitiony vůbec vytvářet.

{{< figure align=center width=200 src="../fsdirect.png" title="FS přímo v disku" >}}

V běžných počítačích se většinou partitiony nachází. OS často izolují partitiony pro svoje vlastní potřeby, do kterých běžný uživatel nemá přístup.

{{< figure align=center width=400 src="../partitionfs.png" title="Partitiony" >}}

Partition systémy lze teoreticky *zanořovat* tzn. jedna partitiona obsahuje vnořený partition systém, v praxi na to ale nikdy nenarazíte, OS toto zanořování podle mě ani neočekávají a neumí s tím pracovat.