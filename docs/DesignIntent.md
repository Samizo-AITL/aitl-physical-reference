---
title: "aitl-physical-reference"
description: "A minimal physical reference PCB that grounds abstract control logic into real voltage, current, and copper."
---

# 🧠 Design Intent

This board provides a **minimal physical reference** that converts  
**abstract control logic** into **observable voltage and current behavior**.

It exists to define the **first physical boundary**  
where logic becomes electricity.

---

## 🎯 Purpose

- 🔌 Anchor logical **ON / OFF** decisions into **real current flow**
- 📍 Provide a **probe-able physical observation point** for control systems
- 🧱 Serve as the **lowest-level physical reference** within the **AITL architecture**

This board intentionally avoids functionality  
and focuses on **grounding**.

---

## 🔗 Relation to AITL

Within **AITL (Architecture for Integrated Technology Logic)**,  
this board represents the **Physical Truth Layer**.

- 🧠 **Logical decision** → 🔌 **Voltage application**
- 🎛 **Control abstraction** → 🟠 **Copper behavior**
- 🧪 **Simulation** → 📏 **Measurable physics**

No firmware.  
No interpretation.  
Only what can be **powered, probed, and measured**.

---

Design intent is preserved by **what is omitted**  
as much as by what is included.

---

## 🟦 v1 Design Intent — Logical ↔ Physical Boundary

**v1** formalizes this board as a  
**logical–physical boundary reference**, not merely a powered artifact.

The intent of v1 is **not to add capability**,  
but to **fix meaning at the boundary**.

---

### 📐 Boundary Definition

In v1, the board explicitly defines:

- 🧠 **Where logic stops**
- 🔌 **Where voltage and current begin**
- 📍 **Where measurement becomes truth**

A single signal — `LOGIC_OUT` — represents this boundary.

> When `LOGIC_OUT` is asserted,  
> the board does not decide *what to do* —  
> it only reveals **what physically happens**.

---

### 🔌 Role of `LOGIC_OUT`

`LOGIC_OUT` is defined as:

- A **logic-originated voltage assertion**
- Free of timing, protocol, or semantic meaning
- Interpreted only through **measured V–I behavior**

`LOGIC_OUT` is **not**:
- a command  
- a control signal  
- a functional abstraction  

It is a **boundary condition**.

---

### 📊 Measurement as Definition

In v1, **measurement defines existence**.

- Voltage confirms logical assertion
- Current confirms physical constraint
- Light confirms observable output

Anything not measurable is **out of scope**.

---

### 🔒 Stability Intent

Once released as v1:

- Electrical meaning of the boundary **shall not change**
- Interpretation belongs to higher layers (FSM / PID / AI)
- This board remains **architecture-agnostic**

Any functional extension must move **outside** this reference.

---

### 🧠 AITL Alignment

Within AITL, v1 corresponds to:

| AITL Layer | Role |
|-----------|------|
| Logic | Decision & abstraction |
| **Physical Reference (this board)** | **Boundary & grounding** |
| Reality | Energy, matter, constraints |

This separation is **intentional and permanent**.

