---
draft: false
title: Jak spustit program? (2.)
weight: 70037
description: Jak spusit program - moderní počítače
---

## Moderní počítače

Procesory a RAM paměti moderních počítačů jsou vždy umístěné na [základní desce]({{< relref "../fyzicka-vrstva/komponenty" >}}). Toto platí pro všechny běžné počítače: stolní počítače, servery, telefony i tablety.

{{< figure align=center width=300 src="../cpurammb1.png" title="Procesor a RAM na základní desce" >}}

Při zapnutí moderního počítače se okamžitě zapne základní deska na které se nachází **napevno zabudovaný miniaturní počítač** --- miniaturní pamět s miniaturním procesorem --- s **jediným spustitelným programem** kterému se říká **bootloader**.

Ten provede následující 3 operace:

1. Vyhledá v celém počítači nějaký spustitelný program. Toto může být napevno přednastavené (např. v telefonech) nebo konfigurovatelné (v běžných počítačích prostřednictvím UEFI, viz. níže).
2. Nalezený program přesune do RAM paměti
3. Spustí procesor a **předá plnou kontrolu nad počítačem procesoru**

{{< figure align=center width=700 src="../cpumbfullmodel.png" title="Bootloader" >}}

<div class="note-blue">
    
⚠️ Hlavním účelem bootloaderu je nalézt v počítači instrukce pro procesor, načíst je do RAM paměti a procesor pustit.

- U běžných počítačů roli bootloaderu zastává **UEFI** nebo starší **BIOS** (o těch bude řeč ještě později).
- Telefony/tablety obsahují zabudované bootloadery na míru udělané výrobcem telefonu.

</div>