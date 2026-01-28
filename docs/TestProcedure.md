# 📏 Test Procedure

This procedure verifies the **logic → physics transition**  
by direct electrical measurement.

---

## 🔌 Power Input

Apply power carefully using a bench supply or probes:

- 🔋 **Supply voltage**: +5.0 V  
- ⏚ **GND**: Connect to board ground  
- ➕ **+5V**: Connect to **R1 input side**

⚠️ Current-limited supply is recommended for first power-on.

---

## 💡 Expected Behavior

With power applied:

- 💡 **LED D1 turns ON** (visible output state)  
- 🔌 **Current flows** through the path:  

```
+5V → R1 → D1 → GND
```

- 📍 **Test Point TP1** shows the **LED forward voltage**

This confirms the physical grounding of a logical ON state.

---

## 📐 Measurement

Measure using a multimeter or probe:

| 📍 Point | 📊 Expected Value |
|--------|------------------|
| 🔋 Supply | 5.0 V |
| 📍 TP1 | ~1.8–2.2 V (LED Vf) |
| 🧮 Current | ~3–5 mA (with 1 kΩ) |

Values are **typical**, not specifications.

---

## 🚫 Failure Cases & Diagnosis

If behavior differs, check the following:

- ❌ **LED OFF**  
→ 🔁 Verify **LED polarity**

- ❌ **0 V at TP1**  
→ 🔍 Open trace or solder joint issue

- ❌ **Full 5.0 V at TP1**  
→ 🔄 LED reversed or not soldered

These checks rely only on **measurement**,  
not interpretation or firmware.

---

If it cannot be measured,  
it does not yet exist in the physical system.
