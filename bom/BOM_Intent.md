---
title: "aitl-physical-reference"
description: "BOM intent defining physical meaning and boundary role of each component."
---

# 🧾 BOM Design Intent

This document defines the **design intent of each BOM item**  
in *aitl-physical-reference*.

The BOM is not a shopping list.  
It is a **declaration of physical meaning**.

---

## 🎯 Purpose of the BOM

- 📏 Fix **electrical and physical meaning** of each component
- 🔒 Preserve **reference equivalence** across builds
- 🧱 Prevent functional drift during reuse or modification

Component values are chosen for **clarity and measurability**,  
not optimization.

---

## 🧩 Component Intent Table

| Ref | Component | Physical Role | Design Intent |
|----|----------|---------------|---------------|
| D1 | LED (0603) | Observable output | Converts current into visible state |
| R1 | 1 kΩ (0603) | Physical constraint | Limits current to safe, measurable range |
| TP1 | Test Point | Observation node | Enables direct voltage probing |
| J1 | Pin Header | Power boundary | Optional external power injection |

Each component exists to answer a **single physical question**.

---

## 🔍 Detailed Intent

### 💡 D1 — LED (0603)

- Represents a **binary physical output**
- Chosen for:
  - Clear visibility
  - Predictable forward voltage
- Color is **non-semantic**

The LED does not *signal meaning*.  
It reveals **energy flow**.

---

### 🧮 R1 — Resistor 1 kΩ (0603)

- Defines the **current constraint**
- Selected to:
  - Keep LED current in a safe, measurable range
  - Avoid thermal or brightness optimization

Changing R1 changes **physical truth**,  
not performance.

---

### 📍 TP1 — Test Point (1.0 mm Pad)

- Provides **direct access** to the physical node
- Exists solely for measurement
- Has no electrical function beyond exposure

If a node cannot be probed,  
it is not part of the reference.

---

### 🔌 J1 — Pin Header (1×02, 2.54 mm)

- Defines the **power boundary**
- Optional by design
- May be replaced by probes without loss of meaning

J1 introduces **no logic**,  
only accessibility.

---

## 🚫 What the BOM Intentionally Excludes

- ❌ Active devices (MCU, logic ICs)
- ❌ Protection circuits (ESD, TVS)
- ❌ Signal conditioning (filters, buffers)
- ❌ Redundant indicators

Absence is part of the design.

---

## 🔒 Stability Rule (v1)

Once released as **v1**:

- Component roles **shall not change**
- Value changes require **new versioning**
- Functional additions belong to **v2 or another board**

The BOM defines **what this board is allowed to be**.

---

## 🧠 AITL Alignment

Within AITL:

- Logic defines *intent*
- BOM fixes *physical consequence*
- Measurement confirms *existence*

The BOM is the **contract between abstraction and matter**.
