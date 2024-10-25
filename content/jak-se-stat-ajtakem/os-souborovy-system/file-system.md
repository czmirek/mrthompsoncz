---
draft: false
title: Souborový systém
weight: 303000
---

Souborový systém (angl. **file system** a velmi často jen zkráceně **fs**) je bitová struktura, díky které na nějakém uložišti vzniká [souborový strom]({{< relref "file-tree" >}}).

{{< figure align=center width=550 src="../filesystem.png" title="Souborový systém" >}}

Souborový systém má dvě hlavní části:

- **index** = index si lze představit jako "Obsah" v knize. Index obsahuje seznam všech cest a také přesně vymezuje, v jakých **blocích** (viz. níže) se soubor nachází.
- **obsah** = obsah je prostor oddělovaný na **bloky** jejichž velikost je u většiny souborových systémů 4 kB. [^b]

## Nejpoužívanější souborové systémy

- `NTFS` - Windows OS
- `ext4` - Linuxové distribuce
- `FAT32` - starší fs, často používaný na obyč. USB flash paměti

[^b]: *Bloky mohou mít i jinou velikost ale to není pro běžného ajťáka podstatné.*