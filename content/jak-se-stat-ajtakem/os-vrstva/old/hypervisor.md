---
draft: true
title: Hypervisor
weight: 2040
---

Moderní procesory mají ještě virtualizační režim. Tento režim je nad privilegovaným režimem. To znamená, že operační systém nemá přístup k instrukcím ve virtualizačním režimu.

![Hypervisor](/jak-se-stat-ajtakem/os-vrstva/hypervisor.png)

Aplikacím, které běží ve virtualizačním režimu se říká hypervisory a to jsou aplikace, které jsou schopné vytvářet a spouštět virtuální zařízení na jednom fyzickém zařízení. To znamená, že na jednom fyzickém zařízení může být provozováno několik virtuálních počítačů, každý se svým vlastním OS.


![Hypervisor 2](/jak-se-stat-ajtakem/os-vrstva/hypervisor2.png)

## Shrnutí

- Hypervisor je program, který umožňuje instalovat virtuální zařízení na fyzické zařízení. Hypervisor běží ve virtualizačním režimu procesoru, ke kterému operační systém ve virtuálním zařízení nemá přístup.