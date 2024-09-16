---
draft: false
title: Sběrnice
weight: 801
---

Sběrnice (anglicky "*bus*") je bitový kanál sloužící pro komunikaci mezi procesorem, RAM pamětí, chipsetem základní desky a všemi ostatními komponentami (vstupy a výstupy) v počítači.

{{< figure align=center width=700 src="../sbernice2.png" title="Sběrnice" >}}

## 3 tradiční typy sběrnic

Tradičně se v IT učebnicích a zdrojích mluví o 3 typech sběrnic které propojují všechny komponenty napříč celým počítačem.

Uvádí se tyto 3 typy sběrnic.

- **Adresová sběrnice**: Toto je sběrnice která posílá informace o **adresách** tzn. **odkud a kam** se mají bity v datové sběrnici posílat.
- **Datová sběrnice**: Toto je sběrnice která posílá samotná data na adresy určené **adresovou sběrnicí**.
- **Řídící sběrnice**: Tato sběrnice určuje, jaká datová operace právě probíhá tzn.: zápis či čtení.

## Realita v moderních počítačích

### Spousta různých sběrnic

V počítačích je spousta různých na sobě nezávislých sběrnic, které moderní procesory dokáží obsluhovat nezávisle na sobě. Tyto sběrnice slouží různým účelům a fungují na různých rychlostech.

Nejznámější typy sběrnic:

- **PCI, PCIe**: sběrnice pro zapojení komponenty postavené jako integrovaný obvod přímo do základní desky
- **SATA**: sběrnice pro kabelové zapojení persistentních uložišť (SSD, HDD)
- **USB**: multifunkční sběrnice pro připojení všeho možného většinou přes USB kabel 

### Chipset základní desky

Funkcionalita sběrnic propojující jednotlivé komponenty připojené k základní desce je závislá jak na procesoru tak i na *chipsetu základní desky*.

Chipset základní desky není žádná konkrétní komponenta ale souhrn různých, na sobě závislých i nezávislých čipů které na základní desce mají různé zodpovědnosti za zprostředkování komunikace mezi komponentami.

### Memory controller

Komunikace mezi procesorem a RAM pamětí je tak důležitá že má svoji vlastní sběrnici tzn. moduly RAM paměti nezapojíte nikam jinam než do určených zásuvek na základní desce dedikovaných přímo pro RAM paměť.

Historicky byla komunikace mezi procesorem a RAM pamětí řízena samostatným čipem nazvaným *memory controller*. V moderních počítačích je však *memory controller* zabudovaný přímo v procesorech. 

### Pro běžného ajťáka toto není podstatné

Komunikace mezi procesorem, RAM pamětí, chipsetem základní desky a všemi ostatními komponentami napříč všemi možnými sběrnicemi je řízena obrovským množstvím různých specifických systémů které se skládají z dalších dílčích subsystémů a podobně.

⚠️ **Důležité k zapamatování:** Tyto obrovské složitosti tvořené všemi možnými mezinárodní korporáty zabývající se IT a výrobou počítačové techniky *(Intel, AMD, NVIDIA, atd.)* je lepší nechat na autorech operačních systémů. Běžný ajťák se těmito tématy zpravidla nezabývá.