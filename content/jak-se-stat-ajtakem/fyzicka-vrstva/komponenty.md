---
draft: false
title: Běžné komponenty
weight: 230
description: Jaké komponenty se nachází v běžných počítačích
---

## Zdroj

{{< figure align=center width=200 src="../psu.png" title="Zdroj pro stolní počítače" >}}
{{< figure align=center width=200 src="../serverpsu.png" title="Zdroj pro servery" >}}

Anglicky se zdroj označuje jako **PSU** (z *Power Source Unit*).

Zdroj je součást počítače, která obsahuje AC/DC převodník (střídavý -> stejnosměrný proud) a napájí elektřinou ostatní komponenty. U mobilních telefonů/tabletů je přítomná baterie, která již poskytuje stejnosměrný proud a převodník pro nabíjení se nachází v nabíječkách.

U stolních počítačů je nutné zajistit zdroj **s dostatečným výkonem**.

Výkon se měří ve **wattech** [^1]. Funkční počítač musí mít zdroj takový, aby pokryl výkon všech svých komponent.

Příklad:
- Základní deska = 10 W
- Procesor = 40 W
- RAM paměť = 15 W

Pro takový počítač musíme mít zdroj s výkonem minimálně 65 W.

## Základní deska

Základní deska (anglicky motherboard) je integrovaný obvod do kterého jsou zasazené všechny komponenty. V nějaké podobě je přítomná ve všech běžných počítačích.

Základní deska všechny komponenty spojuje a bez ní běžný počítač nemůže fungovat.

{{< figure align=center width=200 src="https://upload.wikimedia.org/wikipedia/commons/b/b7/Computer-motherboard.jpg" title="Základní deska pro stolní počítače" >}}
{{< figure align=center width=80 src="../phonemb.png" title="Základní deska telefonu" >}}

## ❗Procesor

❗Procesor je srdcem a mozkem celého počítače a určuje, že zařízení může fungovat jako počítač. 

❗Počítač bez procesoru není počítač a nemůže jako počítač fungovat.

❗**Porozumění procesoru je pro běžného ajťáka klíčové!** Věnuji se mu v dalších kapitolách.

{{< figure align=center width=220 src="../cpu.png" title="Procesor" >}}

## RAM paměť

Každý běžný počítač musí mít **aspoň nějakou** RAM paměť jelikož veškerý **běžící** software se musí nacházet v RAM paměti.

RAM paměť je:

- živá paměť, se kterou je procesor neustále aktivně propojený a kde ukládá data, která pro svoji práci potřebuje
- extrémně rychlá avšak za cenu toho, že veškeré informace z této paměti se ztratí, jakmile se počítač vypne

{{< figure align=center width=210 src="../rampc.png" title="RAM moduly do stolního PC" >}}
{{< figure align=center width=250 src="../ramphone.png" title="RAM v telefonu (ve formě napevno zabudovaného čipu)" >}}


## Persistentní [^2] uložiště

Perzistentní uložiště je jakákoliv komponenta, která si **pamatuje data i po odpojení od elektrického proudu**. Pro tento účel se používají:

### HDD

HDD neboli *hard drive* jsou uložiště, která drží data na kovových plotnách ve formě miniaturních rozdílů v magnetické polaritě. HDD jsou mnohem pomalejší než SSD (viz. níže) ale extrémně levné.

{{< figure align=center width=210 src="../hdd.png" title="HDD do stolního PC" >}}

### Flash (včetně SSD)

Běžně známe *flešku* jako to malé drobné zařízení, na které si může ukládat fotky. 

{{< figure align=center width=210 src="../flashusb.png" title="Flash USB" >}}


Běžný ajťák by však měl vědět, že *flash paměť* je označení pro širokou škálu různých technologií, které fungují na stejném principu - informace jsou uloženy ve formě elektrického náboje ve speciálním materiálu, ve kterém je náboj zachován i po odpojení zařízení z elektřiny.

Mezi tyto technologie patří:

- **SSD**: notebooky, stolní počítače, servery. Mnohonásobně rychlejší, než HDD.

{{< figure align=center width=210 src="../ssd.png" title="SSD disk" >}}

- **SD, mini SD, micro SD**
  - *micro SD* se dnes běžně používají v telefonech a tabletech

{{< figure align=center width=250 src="../sdvariants.png" title="SD varianty" >}}

- **SSD M.2**: nejrychlejší a nejmodernější varianta SSD disků

{{< figure align=center width=300 src="../ssdm2.png" title="SSD M.2" >}}

- **Flash disk**: toto jsou tradiční *fleshky*. Nejsou nijak závratně rychlé ale jsou praktické a velmi levné.

{{< figure align=center width=150 src="../simpleflash.png" title="Flash disk" >}}


## Grafický výstup

Běžné počítače mají nějaký grafický výstup tzn. konektor ke kterému je možné připojit monitor. Servery často žádný grafický výstup nemají.

Počítače s grafickým výstupem mají buď:

- **integrovaný grafický čip** (včetně konektoru) přímo na základní desce.
- nebo **grafickou kartu** připojenou k základní desce. Konektor je na grafické kartě.

Pro potřeby běžného ajťáka **naprosto stačí integrovaný grafický čip**.

{{< figure align=center width=150 src="../gpu.png" title="Grafická karta" >}}

## Síťová karta

Pro komunikaci s jinými zařízeními v síti a pro připojení k internetu je na fyzické úrovni nutné, aby v počítači byla přítomná ethernetová síťová karta.

Počítačovými sítěmi se však budu zabývat až mnohem později.

{{< figure align=center width=300 src="../nic.png" title="Síťová karta" >}}

## Klávesnice, myš, dotyková obrazovka

Běžný ajťák pracuje s klávesnicí a myší, někdy i s dotykovou obrazovkou.

{{< figure align=center width=200 src="../keymou.png" title="Klávesnice a myš" >}}

[^1]: *Výkon se vypočte jako napětí krát proud. Např. `2V * 5A = 7.5W`. U většiny komponent je výkon vždy uvedený nebo dohledatelný.* 
[^2]: *Persistentní = trvalé. V IT toto slovo téměř vždy znamená "informace, která je nějakým způsobem zachována". Na fyzické úrovni to znamená "zachována i po odpojení z elektřiny".*