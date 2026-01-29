---
title: "aitl-physical-reference"
description: "A minimal physical reference PCB that grounds abstract control logic into real voltage, current, and copper."
---

# 🛠 Assembly Guide

This guide describes the **minimal and observable assembly process**  
for the *aitl-physical-reference* PCB.

---

## 🔧 Required Tools

Prepare the following basic tools before assembly:

- 🔥 **Soldering iron** (fine tip recommended)
- 🧷 **Tweezers** (for 0603 handling)
- 🧪 **Flux** (improves solder wetting)
- 📏 **Multimeter** (continuity / voltage check)

No specialized equipment is required.

---

## 🧩 Assembly Steps

Follow the steps in order to maintain clarity and avoid rework.

1. 🧮 **Solder R1** (0603 resistor)  
   - Acts as the **current-limiting physical constraint**

2. 💡 **Solder D1** (LED)  
   - ⚠️ Pay attention to **polarity**  
   - Align the **cathode marking** with the PCB symbol

3. 📍 **Solder TP1** (Test Point Pad)  
   - Provides a **direct voltage observation point**

4. 🔌 **(Optional) Solder J1** (Power Header)  
   - Used for external **+5V / GND** supply connection  
   - May be omitted if power is supplied via probes

---

## 👁 Visual & Electrical Check

After assembly, perform the following checks:

- ✅ No solder bridges between pads  
- ✅ LED orientation is correct  
- ✅ Test point is **not shorted to GND**  
- 🔍 Electrical path should be:

```
+5V → R1 → D1 → GND
```

- 📏 Continuity through **R1 + D1 path only**

These checks ensure a clean **logic → physics mapping**  
before power is applied.

---

Assembly is intentionally simple.  
If something feels “too clever,” it is probably unnecessary.

---

## 🟦 v1 Assembly Intent — Boundary Preservation

Assembly in **v1** must preserve the board’s role as a  
**logical–physical boundary reference**.

The goal is **not correctness of function**,  
but **clarity of physical meaning**.

---

### 🔌 Boundary Awareness During Assembly

When assembling v1, keep the following intent in mind:

- Components do **not** implement logic  
- They only **expose physical consequences** of logic
- Orientation, placement, and solder quality affect **measurement truth**

This board must remain **boringly obvious**.

---

### 📛 Boundary Signal Consideration

If a boundary pin or pad labeled `LOGIC_OUT` is present:

- Treat it as a **pure voltage injection point**
- Do not add pull-ups, filters, or protection circuits
- Do not reinterpret it as a “control signal”

`LOGIC_OUT` exists only to answer:

> *What voltage and current appear in copper  
> when logic asserts a state?*

---

### 🚫 What NOT to Add (v1 Rule)

During assembly, **do not**:

- ❌ Add wires, bodges, or jumpers  
- ❌ Change resistor value “to make it brighter”  
- ❌ Stack components or piggyback parts  
- ❌ Optimize for visibility or aesthetics  

Any such change breaks **reference equivalence**.

---

### 🔒 Assembly Stability Rule

Once assembled as v1:

- The physical meaning of each part **must not change**
- Rework is allowed **only to restore original intent**
- Any enhancement belongs to **v2 or another board**

Assembly errors are corrected.  
Design intent is not negotiated.

---

### 🧠 AITL Alignment

Within AITL, assembly corresponds to:

- 🧠 Logic: already decided elsewhere  
- 🛠 Assembly: fixes meaning into matter  
- 📏 Measurement: confirms existence  

Assembly is where **abstraction becomes irreversible**.

