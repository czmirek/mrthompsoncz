---
draft: false
title: Binární formát programu
weight: 200410
---

Programy jsou jen obyčejné soubory obsahující nějaká binární data, které operační systém dokáže interpretovat jako programy a spustit je.

Tato binární data jsou ve formátu, **který je různý napříč OS** a z toho důvodu není možné aplikace na jeden OS spouštět i na jiném OS.

<div class="note-blue">

⚠️ **Důležité k zapamatování**: Binární formát programu je standard, podle kterého je OS schopný daný program spustit. Každé OS podporuje svůj vlastní standard a z toho důvodu není možné aplikace fungující na jednom OS pouštět na jiném OS.

</div>

## Nejpoužívanější standardy binárních formátů

- **Windows**: [Portable Executable (PE)](https://en.wikipedia.org/wiki/Portable_Executable), PE32+
- **Linuxové distribuce**: [Executable and Linkable Format (ELF)](https://en.wikipedia.org/wiki/Executable_and_Linkable_Format),
- **macOS + iOS**: [Mach-O](https://en.wikipedia.org/wiki/Mach-O)
- **Android**: [Android Package (APK)](https://en.wikipedia.org/wiki/Apk_(file_format)), [Android App Bundle (AAB)](https://en.wikipedia.org/wiki/Android_App_Bundle).