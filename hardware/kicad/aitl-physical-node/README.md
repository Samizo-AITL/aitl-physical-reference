# 🔩 aitl-physical-node

**AITL Physical Node (KiCad Implementation)**  
This directory contains a *physical node implementation* within the  
**AITL (Architecture for Integrated Technology Logic)** framework.

---

## 🧠 What is this?

`aitl-physical-node` represents a **concrete hardware node** that realizes
the *physical truth* assumed by higher-level control and logic layers.

It is **not a reference definition**, but a **deployable instantiation**.

> 🧱 *Reference defines truth*  
> 🔩 *Node realizes truth*

---

## 🏗 Position in AITL Architecture

```
┌───────────────────────────────┐
│   Logic Layer (LLM / Policy)   │
└───────────────▲───────────────┘
                │
┌───────────────┴───────────────┐
│   Control Layer (FSM / PID)    │
└───────────────▲───────────────┘
                │
┌───────────────┴───────────────┐
│ 🔩 Physical Node (THIS)        │
│   Sensors / Actuators / Power  │
└───────────────────────────────┘
```

This node **does not decide**  
This node **does not optimize**  
This node **does not infer**

It simply **behaves according to physics**.

---

## 📂 Contents

| File | Description |
|----|----|
| `aitl-physical-node.kicad_sch` | 🧩 Schematic defining physical connections |
| `aitl-physical-node.kicad_pcb` | 🧭 PCB layout realizing the schematic |
| `aitl-physical-node.kicad_pro` | 📦 KiCad project file |
| `fp-info-cache/` | 📌 KiCad footprint cache |

---

## 🎯 Design Philosophy

- ❌ No abstraction leakage  
- ❌ No control intelligence  
- ❌ No optimization assumptions  

- ✅ Deterministic behavior  
- ✅ Physically explainable signals  
- ✅ Stable reference for control design  

This node exists so that:

> **PID can trust physics**  
> **FSM can trust state transitions**  
> **LLM can trust reconfiguration boundaries**

---

## 🔗 Related

- 📐 [`aitl-physical-reference`](../aitl-physical-reference/)  
  *Defines physical truth*

- 🧠 `aitl-control-reference`  
  *Defines what control means*

---

## ⚠ Notes

- This design may be **simplified, duplicated, or extended**
- Do **not** modify it to embed control logic
- Treat it as **replaceable hardware**, not intelligence

---

## 🧩 AITL Principle (Physical Layer)

> *Reality first.  
> Control second.  
> Intelligence last.*
