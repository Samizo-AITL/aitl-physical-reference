---
title: "aitl-control-reference"
description: "A control architecture reference that defines FSM and PID roles grounded to physical truth."
---

# 🎛 aitl-control-reference

This repository provides a **control architecture reference**  
within the **AITL (Architecture for Integrated Technology Logic)** framework.

It defines **what control means**,  
not how optimized, fast, or intelligent it is.

This project exists to **fix responsibility, structure, and observability**  
of control systems before implementation details are considered.

---

## 🎯 Purpose

The purpose of this repository is **not implementation**, but **definition**.

- 🧭 Define **control roles** (FSM vs PID)
- 🔗 Bind control outputs to **physical truth**
- 📏 Ensure control behavior is **observable and explainable**
- 🧱 Provide a **stable reference** reusable across systems

This repository depends on physical grounding provided by:

- 👉 **`aitl-physical-reference`**

---

## 🧠 Relation to AITL

Within AITL, this repository represents the **Control Reference Layer**.

| AITL Layer | Responsibility |
|-----------|----------------|
| Reasoning | Strategy, redesign, adaptation |
| **Control Reference (this repo)** | **FSM / PID structure and responsibility** |
| Physical Reference | Voltage, current, copper, measurement |

This layer does **not** reason  
and does **not** implement hardware truth.

---

## 📌 Status

### 🟢 v0 — Experimental Control Reference

**v0** represents the **exploratory phase**.

Characteristics:
- FSM and PID may coexist without strict separation
- Control logic may be mixed or simplified
- Structure may change freely
- Intended for **experimentation and understanding**

v0 answers:
> *“What kind of control structure might work?”*

v0 is **allowed to be messy**.

---

## 🟦 v1 Definition — Control Architecture Reference

**v1** formalizes this repository as a  
**control architecture reference**, not an implementation showcase.

This version fixes **what control means**,  
not how fast, smart, or optimal it is.

---

### 🎯 Purpose of v1

- 🎛 Define **clear responsibility separation** between FSM and PID
- 🔗 Bind control outputs to **physical reality via physical-reference**
- 📏 Make control behavior **observable, explainable, and reproducible**

v1 answers one question only:

> *“What is control, and where does each role end?”*

---

### 🧠 Control Architecture Scope (v1)

v1 is strictly architectural.

**Included**
- 🧭 **FSM (Finite State Machine)**  
  - Mode selection  
  - State transitions  
  - Supervisory decisions
- 📐 **PID (or equivalent continuous controller)**  
  - Continuous variable control  
  - Stability and response shaping
- 🔌 Explicit dependency on **`aitl-physical-reference`** for I/O grounding

**Explicitly excluded**
- ❌ Hardware optimization
- ❌ Performance tuning
- ❌ Application-specific logic
- ❌ AI / LLM-based redesign

---

### 🧩 Responsibility Separation

| Layer | Responsibility |
|------|----------------|
| FSM | Discrete mode and state decisions |
| PID | Continuous control within a mode |
| Physical Reference | Voltage, current, and physical truth |

No layer overlaps responsibility.

---

### 🔗 Relation to Physical Reference

All control outputs and observations in v1:

- MUST terminate at **`aitl-physical-reference`**
- MUST be explainable in **voltage, current, and measurement**
- MUST avoid abstract-only signals

If it cannot be measured physically,  
it is **out of scope** for v1.

---

### 📊 Observability Rule

In v1:

- FSM state must be **externally identifiable**
- PID output must be **physically observable**
- Control intent must be visible **without firmware inspection**

Control exists **only when it is observable**.

---

### 🔒 Stability Rule

Once released as v1:

- Architectural roles **shall not change**
- FSM / PID separation **shall not blur**
- Physical dependency **shall remain explicit**

Extensions must become **v1.x** (documentation only)  
or move to **v2**.

---

## 🏷 Versioning Summary

- 🟢 **v0** — Experimental / exploratory control reference
- 🔵 **v1** — Control architecture reference (this definition)
- 🟣 **v2** — Adaptive or AI-assisted control (future)

---

## 🌍 Usage Context

This control reference may be used for:

- 🎛 Control system design studies
- 🧠 FSM / PID role education
- 🔁 Architecture validation with physical reference
- 🤖 AITL-based control discussions

It is **not** a controller, firmware, or product.

---

## 👤 Author

| Item | Details |
|-----|--------|
| **Name** | Shinichi Samizo |
| **GitHub** | https://github.com/Samizo-AITL |

---

## 📄 License

This repository follows the same **hybrid license policy**  
as other AITL reference projects.

Refer to the root license declaration for details.
