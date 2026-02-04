---
title: "KiCad Hardware Sources"
description: "Authoritative KiCad source hierarchy for the AITL physical reference boards."
---

# 🧩 hardware / kicad — KiCad Source Hierarchy

This directory contains the **authoritative KiCad source files**
for all physical reference boards in the
**aitl-physical-reference** project.

These designs define **physical truth**:
real copper, real voltage, real current, and explicit boundaries.

Nothing in this directory is illustrative or symbolic.
Everything here is **manufacturable or intentionally constrained**.

---

## 🎯 Design Philosophy

The KiCad sources in this directory follow three strict rules:

1. **Physical meaning over functionality**  
   Designs exist to define *what physics looks like*, not to perform tasks.

2. **Explicit boundaries**  
   Board outlines (`Edge.Cuts`), current paths, and observability points
   are always explicit and intentional.

3. **Versioned physical semantics**  
   Each subproject represents a stable architectural role.
   Meaning must not drift across versions.

---

## 📂 Directory Structure

```
hardware/kicad/
├─ aitl-physical-loop/ # v2: Executable physical current loop (ground truth)
├─ aitl-physical-node/ # Node-level physical reference (future / optional)
└─ README.md # This file
```

---

Each subdirectory is a **self-contained KiCad project**
with its own README defining **architectural role and stability rules**.

---

## 🟣 aitl-physical-loop (v2)

**Executable Physical Loop Reference**

- Defines a **single closed V–I loop**
- Fully **DRC clean**
- Explicit **Edge.Cuts** (manufacturable boundary)
- Observable without disturbing the loop

This board is the **last layer before control exists**.

📁 Source:

hardware/kicad/aitl-physical-loop/


📖 Local README:

hardware/kicad/aitl-physical-loop/README.md

---

## 🔵 Relationship to Project Versions

| Version | Role |
|------|------|
| v0 | Passive physical reference |
| v1 | Logical ↔ physical boundary definition |
| **v2** | **Executable physical loop (this directory)** |
| v3 | Control insertion reference (FSM / PID) |

The KiCad sources here are **normative for v2**.

---

## 🖼 Figures and Visualization

All schematics, PCB layouts, and 3D renders derived from these KiCad projects
are **canonically indexed and published** on GitHub Pages:

👉 **Figure Index (v0–v2)**  
https://samizo-aitl.github.io/aitl-physical-reference/docs/img/

**Do not duplicate images** inside KiCad directories.
The Pages site is the **single source of visual truth**.

---

## 🔒 Stability Rule

Once a board version is released:

> **Its physical topology and V–I meaning SHALL NOT change.**

Any modification that alters:
- current paths
- constraint elements
- observability points
- board outline

**must advance the major version**.

---

## 🚫 What This Directory Is NOT

- ❌ Not firmware
- ❌ Not MCU-centric
- ❌ Not performance-optimized
- ❌ Not application-specific
- ❌ Not a demo playground

This directory exists to **freeze physical meaning**.

---

## 🔧 Toolchain

- **CAD**: KiCad 9.x
- **Design priority**: Clarity, observability, manufacturability
- **Outputs**: Standard Gerber / drill data

---

## 🔗 Top-Level Context

- Project overview (README):  
  https://samizo-aitl.github.io/aitl-physical-reference/

- Design intent:  
  https://samizo-aitl.github.io/aitl-physical-reference/docs/DesignIntent.html

---

## 👤 Author

**Shinichi Samizo**  
Semiconductor devices, mixed-signal systems, physical–logical architecture

GitHub: https://github.com/Samizo-AITL
