---
title: "aitl-physical-reference"
description: "Test procedure verifying logic-to-physics grounding by direct V–I measurement."
---

# 📏 Test Procedure

This procedure verifies the **logic → physics transition**  
by **direct electrical measurement**.

If it cannot be measured,  
it does not yet exist in the physical system.

---

## 🔌 Power Input (v0 / v1 Common)

Apply power carefully using a bench supply or probes:

- 🔋 **Supply voltage**: +5.0 V  
- ⏚ **GND**: Connect to board ground  
- ➕ **+5V**: Connect to **PWR_IN / R1 input side**

⚠️ A current-limited supply is recommended for first power-on.

---

## 💡 Expected Behavior (v0 Passive Reference)

With power applied:

- 💡 **LED D1 turns ON** (visible physical output)  
- 🔌 **Current flows** through the path:

```
+5V → R1 → D1 → GND
```

- 📍 **Test Point TP1** shows the **LED forward voltage**

This confirms the **existence of a physical ON state**,  
independent of logic or firmware.

---

## 📐 Measurement (v0)

Measure using a multimeter or probe:

| 📍 Point | 📊 Expected Value |
|--------|------------------|
| 🔋 Supply | 5.0 V |
| 📍 TP1 | ~1.8–2.2 V (LED Vf) |
| 🧮 Current | ~3–5 mA (with 1 kΩ) |

Values are **typical**, not specifications.

---

## 🚫 Failure Cases & Diagnosis (v0)

- ❌ **LED OFF**  
  → 🔁 Verify **LED polarity**

- ❌ **0 V at TP1**  
  → 🔍 Open trace or solder joint issue

- ❌ **Full 5.0 V at TP1**  
  → 🔄 LED reversed or not soldered

These checks rely only on **measurement**,  
not interpretation, firmware, or intent.

---

## 🟦 v1 Boundary Verification — Logical ↔ Physical

This section verifies the **logical–physical boundary behavior**  
defined in **v1**.

Here, logic does not *control* the system —  
it only **asserts a voltage level at the boundary**.

---

### 🔌 Test Conditions (v1)

- Power supply: **+5.0 V ±5%**
- Measurement tools: DMM (voltage / current)
- Logic source: External GPIO, jumper, or signal generator
- Boundary pin: **`LOGIC_OUT`**

---

### 📊 Measurement Items (v1 Normative)

| ID | Node | Condition | Expected Result |
|----|------|-----------|----------------|
| TP-01 | VCC | Power ON | 5.0 V ±5% |
| TP-02 | LOGIC_OUT | Logic = High | 3.3–5.0 V |
| TP-03 | LED_NODE | LOGIC_OUT = High | Vf = 1.8–2.2 V |
| TP-04 | LED Current | LOGIC_OUT = High | 5–10 mA |

This table is **normative** for v1.

---

### ✅ Pass Criteria (v1)

- LED turns ON/OFF corresponding **only** to `LOGIC_OUT`
- Measured voltage/current remains within expected range
- No unintended current flow when `LOGIC_OUT = Low`

Passing these checks confirms that:

> **Logical intent is faithfully translated  
> into physical voltage and current.**

---

### 🔒 Interpretation Rule

This procedure verifies **reality**, not correctness.

- No timing is implied  
- No control quality is assumed  
- No intelligence is evaluated  

Only **V–I existence and observability** are validated.
