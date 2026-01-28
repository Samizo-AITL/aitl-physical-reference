# 🧩 aitl-physical-reference

This repository provides a **minimal physical reference PCB**  
that anchors abstract control and logic concepts into **real voltage, current, and copper**.

It is intentionally **small, generic, and architecture-agnostic**,  
focusing on **observability, physical constraints, and manufacturability** rather than functionality.

[![Back to Portal (EN)](https://img.shields.io/badge/Back%20to%20Portal-0B5FFF?style=for-the-badge&logo=homeassistant&logoColor=white)](https://samizo-aitl.github.io/portal/en/)

---

## 🔗 Links

| Language | GitHub Pages 🌐 | GitHub 💻 |
|----------|----------------|-----------|
| 🇺🇸 English | [![GitHub Pages EN](https://img.shields.io/badge/GitHub%20Pages-English-brightgreen?logo=github)](https://samizo-aitl.github.io/aitl-physical-reference/) | [![GitHub Repo EN](https://img.shields.io/badge/GitHub-English-blue?logo=github)](https://github.com/Samizo-AITL/aitl-physical-reference/tree/main) |

---

## 🎯 Purpose

The purpose of this board is **not control**, but **grounding**.

- 🔌 Fix abstract logic into **measurable V–I behavior**
- 👁 Provide a **visible and probe-able physical endpoint**
- 🧱 Act as a **lowest-level physical reference**, reusable across systems

This board can be *used by* higher-level architectures  
(control logic, supervisory layers, AI reasoning),  
but it **does not depend on them**.

---

## 🧩 What This Is

This repository contains a **reference PCB**, not a product.

The board includes only elements required to expose  
the relationship between logic and physics:

- 💡 **LED** — observable output state  
- 🧮 **Resistor** — physical constraint (current limitation)  
- 🔘 **Switch** — discrete physical event input  
- 📍 **Test Point** — voltage / current measurement access  
- 📐 **Board outline (Edge.Cuts)** — explicit physical boundary  

Nothing more.

---

## 🖼 Physical Reference Overview

### 1️⃣ Schematic (Logical → Physical Mapping)

![Schematic](https://samizo-aitl.github.io/aitl-physical-reference/docs/img/01_apr_sch_v0.png)

This schematic shows the **minimal logic-to-physics mapping**:  
LED, resistor, switch, and test point only — nothing abstracted away.

---

### 2️⃣ PCB Layout (Physical Constraints)

![PCB Layout](https://samizo-aitl.github.io/aitl-physical-reference/docs/img/02_apr_pcb_v0.png)

The PCB layout explicitly exposes:

- 🟠 Copper routing  
- 📦 Component placement  
- ⛓ Board boundary (Edge.Cuts)  

This is the **physical truth layer**.

---

### 3️⃣ 3D View (Embodied Reality)

![3D View](https://samizo-aitl.github.io/aitl-physical-reference/docs/img/03_apr_3d_v0.png)

The 3D view represents the **embodiment** of logic:  
real height, real connectors, real probe access.

---

## 🚫 What This Is NOT

- ❌ Not a full controller  
- ❌ Not MCU-centric  
- ❌ Not performance-optimized  
- ❌ Not tied to any single architecture or framework  
- ❌ Not a demo board for features  

This repository intentionally avoids *solutions* and focuses on *reference*.

---

## 🧠 Architecture Mapping (Conceptual → Physical)

| Conceptual Role | Physical Element |
|-----------------|------------------|
| Output state    | 💡 LED           |
| Constraint      | 🧮 Resistor      |
| Event input     | 🔘 Switch        |
| Observation     | 📍 Test point    |
| Boundary        | 📐 PCB outline   |

This mapping is the **core value** of the project.

---

## 🗂 Repository Structure

```
aitl-physical-reference/
├─ hardware/
│ └─ kicad/ # KiCad project (schematic / PCB)
├─ bom/
│ └─ bom.csv # Component list (non-CAD)
├─ docs/
│ ├─ Assembly.md # Assembly instructions
│ ├─ TestProcedure.md # Measurement & verification
│ └─ DesignIntent.md # Physical design intent
└─ README.md
```

---

## 🔧 Build & Assembly Flow

To physically build and use this reference board:

1. 📄 Review **`bom/bom.csv`** and prepare components  
2. 🏭 Manufacture PCB using KiCad data in `hardware/kicad/`  
3. 🛠 Assemble components following **`docs/Assembly.md`**  
4. ⚡ Apply +5V power and observe LED behavior  
5. 📊 Verify voltage/current using **`docs/TestProcedure.md`**

This flow is intentionally simple and repeatable.

---

## 📏 Verification & Measurement

This board is designed to be **measured**, not just powered.

Typical checks:

- 💡 LED ON/OFF state  
- 📍 Forward voltage at test point  
- 🧮 Current limited by resistor  
- 📐 Boundary defined by board outline  

These checks validate the **logic → physics transition**.

---

## 🧰 Toolchain

- 🧩 **CAD**: KiCad  
- 🎨 **Design style**: Minimal, readable, single-layer preferred  
- 📤 **Outputs**: Standard manufacturable Gerber data  

The design favors **clarity over density**.

---

## 🌍 Usage Context

This physical reference can be used in:

- 🎛 Control systems  
- 🧠 Supervisory logic  
- 🎓 Educational hardware  
- 🔁 Logic-to-physical architecture studies  
- 🤖 AITL-based discussions and validation  

It acts as a **ground truth layer**, not a controller.

---

## 📌 Status

- **v0** — Minimal physical reference  
  - 💡 LED  
  - 🧮 Resistor  
  - 🔘 Switch  
  - 📍 Test point  

Future revisions may extend observability,  
but will preserve minimalism.

---

## 🗺 Roadmap

- 🟢 v0: Passive physical reference (LED / R / SW / TP)
- 🔵 v1: MCU boundary reference (GPIO ↔ Physical)
- 🟣 v2: Control-capable reference (PID / FSM execution)

---

## 👤 Author

| 📌 Item | Details |
|--------|---------|
| **Name** | Shinichi Samizo |
| **Expertise** | Semiconductor devices (logic, memory, high-voltage mixed-signal)<br>Thin-film piezo actuators for inkjet systems<br>Printhead productization, BOM management, ISO training |
| **GitHub** | [![GitHub](https://img.shields.io/badge/GitHub-Samizo--AITL-black?logo=github)](https://github.com/Samizo-AITL) |

---

## 📄 License

[![Hybrid License](https://img.shields.io/badge/license-Hybrid-blueviolet)](https://samizo-aitl.github.io/aitl-physical-reference/#---license)

| 📌 Item | License | Description |
|--------|---------|-------------|
| **Source Code** | [**MIT License**](https://opensource.org/licenses/MIT) | Free to use, modify, and redistribute |
| **Text Materials** | [**CC BY 4.0**](https://creativecommons.org/licenses/by/4.0/) or [**CC BY-SA 4.0**](https://creativecommons.org/licenses/by-sa/4.0/) | Attribution required; share-alike applies for BY-SA |
| **Figures & Diagrams** | [**CC BY-NC 4.0**](https://creativecommons.org/licenses/by-nc/4.0/) | Non-commercial use only |
| **External References** | Follow the original license | Cite the original source properly |

---

## 💬 Feedback

> Suggestions, improvements, and discussions are welcome via GitHub Discussions.

[![💬 GitHub Discussions](https://img.shields.io/badge/💬%20GitHub-Discussions-brightgreen?logo=github)](https://github.com/Samizo-AITL/aitl-physical-reference/discussions)

