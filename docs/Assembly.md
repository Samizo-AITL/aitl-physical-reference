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
