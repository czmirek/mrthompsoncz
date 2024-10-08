---
draft: false
title: Běžné komponenty
weight: 230
---

## Zdroj

Důležitou komponentou, které by měl běžný ajťák rozumět (na fyzické, elektrické vrstvě) je **zdroj**. Je to součást počítače, která obsahuje AC/DC převodník a napájí elektřinou všechny ostatní komponenty.

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

## Procesor

❗Procesor je srdcem a mozkem celého počítače a víceméně definuje, že nějaké zařízení může fungovat jako počítač. 

❗Běžný počítač bez procesoru není počítač a nemůže jako počítač fungovat. Toto platí pro všechny běžné počítače:

- mobilní telefony/tablety
- stolní počítače/notebooky
- servery

❗**Porozumění, jak funguje procesor, je pro běžného ajťáka klíčové!** Proto se na procesor budu v rámci tohoto návodu soustředit nejvíce.

## RAM paměť

Pro potřeby běžného ajťáka je nutné, aby každé zařízení, se kterým ajťák potřebuje pracovat, mělo **aspoň nějakou** RAM paměť.

RAM paměť je živá paměť, se kterou je procesor neustále aktivně propojený a kde ukládá data, která pro svoji práci potřebuje.

RAM paměť je extrémně rychlá avšak za cenu toho, že veškeré informace z této paměti se ztratí, jakmile se počítač vypne.

## Persistentní[^2] uložiště

Perzistentní uložiště je jakákoliv komponenta, která si **pamatuje data i po odpojení od elektrického proudu**. Pro tento účel se používají:

### HDD

HDD neboli *hard drive* jsou uložiště, která drží data na kovových plotnách ve formě rozdílů v magnetické polaritě

HDD jsou mnohem pomalejší než SSD (viz. níže) ale extrémně levné.

### Flash (včetně SSD)

Běžný člověk zná "flešku" jako to malé drobné zařízení, na které si může ukládat fotky. 

Běžný ajťák by však měl vědět, že *flash paměť* je označení pro celkem širokou škálu různých technologií, které fungují na stejném principu - informace jsou uloženy ve formě elektrického náboje, který je zachován i po odpojení z elektřiny.

Mezi tyto technologie patří:

- *SD, mini SD, micro SD*
  - *micro SD* se dnes běžně používají v telefonech a tabletech
- *SSD*: notebooky, stolní počítače, servery. Mnohonásobně rychlejší, než HDD.
- *SSD M.2*: nejrychlejší varianta připojená přímo k základní desce

## Grafický výstup

Běžný **fyzický počítač** má nějaký grafický výstup tzn. konektor ke kterému je možné připojit monitor. Takový počítač má buď:

- integrovaný grafický čip (včetně konektoru) přímo na základní desce
- grafickou kartu připojenou k základní desce, konektor je na grafické kartě

Pro potřeby běžného ajťáka **naprosto stačí integrovaný grafický čip**.

## Síťová karta

Pro komunikaci s jinými zařízeními v síti a pro připojení k internetu je na fyzické úrovni nutné, aby v počítači byla přítomná ethernetová síťová karta.

Počítačovým sítím se však budeme zabývat zvlášť jindy.

## Klávesnice a myš

Běžný ajťák pracuje s klávesnicí a myší (někdy i s dotykovou obrazovkou). [^m]

[^1]: *Výkon se vypočte jako napětí krát proud. Např. `2V * 5A = 7.5W`. U většiny komponent je však hodnota ve wattech vždy uvedená nebo dohledatelná.* 
[^2]: *Persistentní = trvalé. V IT toto slovo téměř vždy znamená "informace, která je nějakým způsobem zachována". Na fyzické úrovni to znamená "zachována i po odpojení z elektřiny".*
[^m]: *Někteří běžní ajťáci práci s myší nesnáší ale do těchto diskuzí se zde nechci pouštět.*