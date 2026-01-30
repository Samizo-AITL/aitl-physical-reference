---
title: "aitl-physical-reference"
description: "A minimal physical reference PCB that grounds abstract control logic into real voltage–current behavior and copper."
---

# 🧠 Design Intent

This board provides a **minimal physical reference** that anchors  
**abstract control logic** into **observable voltage–current (V–I) behavior**.

It exists to define the **first physical boundary**  
where logic becomes electricity.

---

## 🎯 Purpose

- 🔌 Anchor logical **ON / OFF** decisions into **real current flow (V–I reality)**
- 📍 Provide a **probe-able observation point** for validation and discussion
- 🧱 Serve as the **lowest-level physical reference** within **AITL (Architecture for Integrated Technology Logic)**

This board intentionally avoids functionality  
and focuses on **grounding**.

---

## 🔗 Relation to AITL

Within **AITL (Architecture for Integrated Technology Logic)**,  
this board represents the **Physical Truth Layer** — the place where:

- 🧠 **Logical decision** → 🔌 **Voltage assertion**
- 🎛 **Control abstraction** → 🟠 **Copper current path**
- 🧪 **Simulation** → 📏 **Measured V–I truth**

No firmware.  
No interpretation.  
Only what can be **powered, probed, and measured**.

Design intent is preserved by **what is omitted**  
as much as by what is included.

---

## 🟦 v1 Design Intent — Logical ↔ Physical Boundary (Normative)

**v1** formalizes this board as a  
**logical–physical boundary reference** — not merely a powered artifact.

The intent of v1 is **not to add capability**,  
but to **fix meaning at the boundary** in a way that higher layers can rely on.

---

### 📐 Boundary Definition

In v1, the board explicitly defines:

- 🧠 **Where logic stops**
- 🔌 **Where voltage and current begin**
- 📍 **Where measurement becomes truth**

A single signal — `LOGIC_OUT` — represents this boundary.

> When `LOGIC_OUT` is asserted,  
> the board does not decide *what to do*.  
> It only reveals **what physically happens** in voltage–current (V–I) terms.

---

### 🔌 Role of `LOGIC_OUT`

`LOGIC_OUT` is defined as:

- A **logic-originated voltage assertion**
- Free of timing, protocol, or functional semantics
- Interpreted only through **measured V–I behavior**

`LOGIC_OUT` is **not**:
- a command  
- a control algorithm  
- a functional abstraction  

It is a **boundary condition**.

---

### 📊 Measurement as Definition

In v1, **measurement defines existence**.

- Voltage measurement confirms **logical assertion**
- Current measurement confirms **physical constraint**
- Light emission confirms **observable output state**

Anything not measurable is **out of scope**.

---

### 🔒 Stability Intent (Normative)

Once released as **v1**:

- Electrical meaning at the boundary **SHALL NOT change**
- Interpretation belongs to higher layers (FSM / PID / AI)
- This board remains **architecture-agnostic and timeless**

Any functional extension must move **outside** this reference:
- documentation-only updates may be **v1.x**
- functional changes must become **v2**

---

### 🧠 AITL Alignment

Within AITL, v1 corresponds to:

| AITL Layer | Role |
|-----------|------|
| Logic | Decision & abstraction |
| **Physical Reference (this board)** | **Boundary & grounding (V–I truth)** |
| Reality | Energy, matter, constraints |

This separation is **intentional** and **permanent**.
