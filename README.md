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

## 📂 Key Artifacts (Reference Entry Points)

### 📄 Documentation
- **Design Intent**  
  [GitHub Page](https://samizo-aitl.github.io/aitl-physical-reference/docs/DesignIntent.html)  
  [Repository](https://github.com/Samizo-AITL/aitl-physical-reference/tree/main/docs/DesignIntent.md)

- **Assembly Instructions**  
  [GitHub Page](https://samizo-aitl.github.io/aitl-physical-reference/docs/Assembly.html)  
  [Repository](https://github.com/Samizo-AITL/aitl-physical-reference/tree/main/docs/Assembly.md)

- **Test & Measurement Procedure**  
  [GitHub Page](https://samizo-aitl.github.io/aitl-physical-reference/docs/TestProcedure.html)  
  [Repository](https://github.com/Samizo-AITL/aitl-physical-reference/tree/main/docs/TestProcedure.md)

### 🧾 Bill of Materials
- **BOM (CSV)**  
  [GitHub Page](https://samizo-aitl.github.io/aitl-physical-reference/bom/bom.csv)  
  [Repository](https://github.com/Samizo-AITL/aitl-physical-reference/blob/main/bom/bom.csv)

### 🧩 Hardware Source (Physical Truth)
- **KiCad Project (Schematic / PCB)**  
  [Repository](https://github.com/Samizo-AITL/aitl-physical-reference/tree/main/hardware/kicad)

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

## 🟦 v1 Definition — Physical ↔ Logical Boundary Reference

**v1** extends *aitl-physical-reference* from a passive grounding board  
into a **clearly defined physical–logical boundary reference**.

This version does **not** aim to control, compute, or decide.  
It exists solely to **define where logic ends and physics begins**.

---

### 🎯 Purpose of v1

- 🔗 Define a **clear GPIO ↔ physical boundary**
- 📏 Fix **measurable voltage–current expectations** at that boundary
- 🧭 Provide a **stable reference point** for higher layers (FSM / PID / AI)

v1 answers one question only:

> *“When logic toggles a pin, what does that mean in copper, voltage, and current?”*

---

### 🔌 v1 Scope (Strict)

v1 **adds a boundary**, not intelligence.

**Included**
- 📍 Explicit **logic-level input/output pins**
- 💡 Physical load (LED + R) driven *through* that boundary
- 📊 Documented **expected V–I ranges per node**
- 🧪 Test points tied to logical meaning

**Explicitly excluded**
- ❌ No firmware logic
- ❌ No control algorithm
- ❌ No timing guarantees
- ❌ No optimization

---

### 📐 Boundary Concept

| Layer | Responsibility |
|------|----------------|
| Logical / MCU | State decision, timing, abstraction |
| **v1 Boundary** | **Voltage level, current flow, observability** |
| Physical | Light emission, heat, copper limits |

v1 is the **line**, not the controller.

---

### 📊 Reference Measurement Table (Normative)

| Node | Condition | Expected Voltage | Expected Current | Meaning |
|-----|----------|-----------------|-----------------|--------|
| LOGIC_OUT | High | 3.3–5.0 V | < 1 mA | Logic asserts state |
| LED_NODE | ON | 1.8–2.2 V | 5–10 mA | Physical output active |
| VCC | Nominal | 5.0 V ±5% | — | Power reference |

This table is **normative** in v1.

---

### 🧠 Architectural Role

v1 serves as:

- 🔹 **FSM** — physical state confirmation point  
- 🔹 **PID** — actuator-side reality reference  
- 🔹 **LLM / AI** — grounding layer to prevent abstraction drift  

Higher layers may change.  
**v1 must not.**

---

### 🔒 Stability Rule

Once released:

> **v1 electrical meaning SHALL NOT change.**

Any extension must:
- become **v1.x** (documentation / measurement only), or
- move to **v2** (control-capable reference)

---

### 🏷 Versioning Summary

- 🟢 **v0** — Passive physical reference (LED / R / SW / TP)
- 🔵 **v1** — Logical–physical boundary reference
- 🟣 **v2** — Control-capable execution reference (FSM / PID)

---

## 🔖 GPIO Naming Rule (v1)

GPIO names in **v1** are **semantic and directional**.  
They describe **what crosses the boundary**, not how it is implemented.

### 📛 Naming Format

```
<ROLE>_<DIRECTION>
```

- **ROLE**: logical meaning at the boundary  
- **DIRECTION**: signal direction *from logic perspective*

### 📌 Standard Roles

| Name | Meaning |
|-----|--------|
| `LOGIC_OUT` | Logic asserts a physical state |
| `LOGIC_IN` | Logic observes a physical condition |
| `PWR_IN` | External power reference |
| `GND` | Electrical ground |

### 🔄 Direction Definition

- `_OUT` : logic → physical  
- `_IN`  : physical → logic  

> Example: `LOGIC_OUT` means  
> “Logic drives voltage/current into the physical layer.”

### 🚫 Prohibited in v1

- ❌ MCU-specific names (`PA0`, `GPIO23`)
- ❌ Functional assumptions (`LED_CTRL`, `PWM_OUT`)
- ❌ Timing semantics (`CLK`, `SYNC`)

v1 names must remain **architecture-agnostic and timeless**.

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

