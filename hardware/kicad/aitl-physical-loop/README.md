---
title: "aitl-physical-loop (KiCad Source)"
description: "KiCad source files for the executable physical loop reference (v2) in the AITL physical reference project."
---

# 🧩 aitl-physical-loop — KiCad Source

This directory contains the **authoritative KiCad source files**
for the **v2 executable physical loop reference** of the
*aitl-physical-reference* project.

This design represents a **closed, manufacturable V–I loop**
that is **DRC-clean, observable, and topology-stable**.

It is **not** a controller, and it contains **no logic or firmware**.

---

## 🎯 Role in the Architecture

| Layer | Meaning |
|------|--------|
| v1 | Logical ↔ physical boundary definition |
| **v2 (this board)** | **Executable physical ground truth** |
| v3+ | Control / supervision / adaptation |

This board answers one question only:

> **“What does a frozen physical current loop look like in real copper?”**

---

## 📂 Contents

| File | Description |
|-----|------------|
| `aitl-physical-loop.kicad_pro` | KiCad project file |
| `aitl-physical-loop.kicad_sch` | Schematic (logical definition of the loop) |
| `aitl-physical-loop.kicad_pcb` | PCB layout (physical realization, Edge.Cuts defined) |
| `aitl-physical-loop.kicad_prl` | KiCad project local settings |
| `fp-info-cache` | KiCad footprint cache |

These files together define the **single source of physical truth** for v2.

---

## 🖼 Reference Figures

All figures derived from this KiCad project
(schematic, PCB layout, 3D view) are **canonically indexed and embedded**
on the following page:

👉 **Figure Index (v0–v2)**  
https://samizo-aitl.github.io/aitl-physical-reference/docs/img/

Referenced figures include:

- **Fig.07** — v2 Schematic  
- **Fig.08** — v2 PCB Layout  
- **Fig.09** — v2 3D View  

Do **not** duplicate images here.  
The figure index is the **single normative reference**.

---

## 🔒 Stability Rule (v2)

Once released:

> **The physical loop topology and its V–I meaning SHALL NOT change.**

Any modification that alters:
- current path,
- constraint elements,
- observability points, or
- board outline

**must advance the version to v3**.

---

## 🚫 What This Is NOT

- ❌ Not a microcontroller board
- ❌ Not GPIO-defined logic
- ❌ Not feedback or control capable
- ❌ Not optimized for size or cost

This directory exists to preserve **physical meaning**, not behavior.

---

## 🔧 Toolchain

- **CAD**: KiCad 9.x
- **Design goal**: Clarity, observability, manufacturability
- **Status**: DRC clean, Edge.Cuts defined

---

## 🔗 Top-Level Context

For project intent, documentation, and measurement procedures, see:

- Project root (README):  
  https://samizo-aitl.github.io/aitl-physical-reference/

- Design intent:  
  https://samizo-aitl.github.io/aitl-physical-reference/docs/DesignIntent.html

---

## 👤 Author

**Shinichi Samizo**  
Semiconductor devices, mixed-signal systems, physical–logical architecture

GitHub: https://github.com/Samizo-AITL
