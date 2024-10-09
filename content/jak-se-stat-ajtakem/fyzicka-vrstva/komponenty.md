---
draft: false
title: Běžné komponenty
weight: 230
---

## Zdroj

Důležitou komponentou, které by měl běžný ajťák rozumět (na fyzické, elektrické vrstvě) je **zdroj**. Anglicky se zdroj označuje jako **PSU** (z *Power Source Unit*).

{{< figure align=center width=200 src="../psu.png" title="Zdroj pro stolní počítače" >}}
{{< figure align=center width=200 src="../serverpsu.png" title="Zdroj pro servery" >}}

Je to součást počítače, která obsahuje AC/DC převodník a napájí elektřinou všechny ostatní komponenty.

Zdroj většinou neřešíte u mobilních telefonů nebo tabletů, ten je tam napevno zabudovaný a zpravidla nelze vyměnit.

U počítačů, které lze stavět jako stavebnice, je nutné vždy zajistit, že v počítači je zdroj **s dostatečným výkonem**.

Výkon se měří ve **wattech**[^1]. Funkční počítač musí mít zdroj takový, aby pokryl výkon všech svých komponent.

Příklad:
- Základní deska = 10 W
- Procesor = 40 W
- RAM paměť = 15 W

Pro takový počítač musíme mít zdroj s výkonem minimálně 65 W.

## Základní deska

Základní deska je integrovaný obvod do kterého jsou zasazené všechny komponenty a je v nějaké podobě přítomná ve všech běžných zařízeních: v mobilních telefonech, tabletech, noteboocích, stolních počítačech i serverech.

Základní deska všechny komponenty spojuje a není bez ní možné, aby běžný počítač fungoval.

{{< figure align=center width=200 src="https://upload.wikimedia.org/wikipedia/commons/b/b7/Computer-motherboard.jpg" title="Základní deska pro stolní počítače" >}}
{{< figure align=center width=80 src="../phonemb.png" title="Základní deska telefonu" >}}

## Procesor

❗Procesor je srdcem a mozkem celého počítače a víceméně definuje, že nějaké zařízení může fungovat jako počítač. 

❗Běžný počítač bez procesoru není počítač a nemůže jako počítač fungovat. Toto platí pro všechny běžné počítače:

- mobilní telefony/tablety
- stolní počítače/notebooky
- servery

❗**Porozumění, jak funguje procesor, je pro běžného ajťáka klíčové!** Proto se na procesor budu v rámci tohoto návodu soustředit nejvíce.

{{< figure align=center width=220 src="../cpu.png" title="Procesor" >}}

## RAM paměť

Pro potřeby běžného ajťáka je nutné, aby každé zařízení, se kterým ajťák potřebuje pracovat, mělo **aspoň nějakou** RAM paměť.

RAM paměť je živá paměť, se kterou je procesor neustále aktivně propojený a kde ukládá data, která pro svoji práci potřebuje.

RAM paměť je extrémně rychlá avšak za cenu toho, že veškeré informace z této paměti se ztratí, jakmile se počítač vypne.

{{< figure align=center width=210 src="../rampc.png" title="RAM moduly do stolního PC" >}}
{{< figure align=center width=250 src="../ramphone.png" title="RAM v telefonu (ve formě napevno zabudovaného čipu)" >}}


## Persistentní[^2] uložiště

Perzistentní uložiště je jakákoliv komponenta, která si **pamatuje data i po odpojení od elektrického proudu**. Pro tento účel se používají:

### HDD

HDD neboli *hard drive* jsou uložiště, která drží data na kovových plotnách ve formě rozdílů v magnetické polaritě. HDD jsou mnohem pomalejší než SSD (viz. níže) ale extrémně levné.

{{< figure align=center width=210 src="../hdd.png" title="HDD do stolního PC" >}}

### Flash (včetně SSD)

Běžný člověk zná "flešku" jako to malé drobné zařízení, na které si může ukládat fotky. 

Běžný ajťák by však měl vědět, že *flash paměť* je označení pro celkem širokou škálu různých technologií, které fungují na stejném principu - informace jsou uloženy ve formě elektrického náboje ve speciálním materiálu. El. náboj je zachován i po odpojení zařízení z elektřiny.

Mezi tyto technologie patří:

- **SSD**: notebooky, stolní počítače, servery. Mnohonásobně rychlejší, než HDD.

{{< figure align=center width=210 src="../ssd.png" title="SSD disk" >}}

- **SD, mini SD, micro SD**
  - *micro SD* se dnes běžně používají v telefonech a tabletech

{{< figure align=center width=250 src="../sdvariants.png" title="SD varianty" >}}

- **SSD M.2**: nejrychlejší a nejmodernější varianta SSD disků

{{< figure align=center width=300 src="../ssdm2.png" title="SSD M.2" >}}

- **Flash disk**: toto jsou tradiční "fleshky". Nejsou nijak závratně rychlé, jsou však praktické a velmi levné.

{{< figure align=center width=150 src="../simpleflash.png" title="Flash disk" >}}


## Grafický výstup

Běžný **fyzický počítač** má nějaký grafický výstup tzn. konektor ke kterému je možné připojit monitor. Takový počítač má buď:

- integrovaný grafický čip (včetně konektoru) přímo na základní desce
- grafickou kartu připojenou k základní desce, konektor je na grafické kartě

Pro potřeby běžného ajťáka **naprosto stačí integrovaný grafický čip**.

{{< figure align=center width=150 src="../gpu.png" title="Grafická karta" >}}

## Síťová karta

Pro komunikaci s jinými zařízeními v síti a pro připojení k internetu je na fyzické úrovni nutné, aby v počítači byla přítomná ethernetová síťová karta.

Počítačovými sítěmi se však budu zabývat až mnohem později.

{{< figure align=center width=300 src="../nic.png" title="Síťová karta" >}}

## Klávesnice a myš

Běžný ajťák pracuje s klávesnicí a myší (někdy i s dotykovou obrazovkou). [^m]

{{< figure align=center width=200 src="../keymou.png" title="Klávesnice a myš" >}}

[^1]: *Výkon se vypočte jako napětí krát proud. Např. `2V * 5A = 7.5W`. U většiny komponent je však hodnota ve wattech vždy uvedená nebo dohledatelná.* 
[^2]: *Persistentní = trvalé. V IT toto slovo téměř vždy znamená "informace, která je nějakým způsobem zachována". Na fyzické úrovni to znamená "zachována i po odpojení z elektřiny".*
[^m]: *Někteří běžní ajťáci práci s myší nesnáší ale do těchto diskuzí se zde nechci pouštět.*