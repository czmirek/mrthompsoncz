---
draft: false
title: "Heap segment: vrácení paměti"
weight: 215000
---

Vrácení paměti je přímočaré.

- Proces sdělí OS API, že už danou položku heapu nepotřebuje a předá adresu, kterou původně od OS API dostal.
- OS API položku uvolní.
- Proces již nemůže adresu jakkoliv využít
