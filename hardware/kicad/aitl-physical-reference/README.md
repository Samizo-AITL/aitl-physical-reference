## 🟦 v1 Definition — Control Architecture Reference

**v1** defines *aitl-control-reference* as a  
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
- 🧭 FSM (Finite State Machine):  
  - Mode selection  
  - State transitions  
  - Supervisory logic
- 📐 PID (or equivalent continuous controller):  
  - Continuous variable control  
  - Stability and response shaping
- 🔌 Explicit dependency on **`aitl-physical-reference`** for I/O grounding

**Explicitly excluded**
- ❌ Hardware optimization
- ❌ Performance tuning
- ❌ Application-specific logic
- ❌ AI/LLM-based redesign

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

v1 requires that:

- FSM state can be **externally identified**
- PID output can be **physically observed**
- Control intent is visible **without firmware inspection**

Control exists only when it is observable.

---

### 🔒 Stability Rule

Once released as v1:

- Architectural roles **shall not change**
- FSM/PID separation **shall not blur**
- Physical dependency **shall remain explicit**

Extensions must become **v1.x** (documentation only)  
or move to **v2**.

---

### 🏷 Versioning Summary

- 🟢 **v0** — Experimental / mixed control
- 🔵 **v1** — Control architecture reference (this section)
- 🟣 **v2** — Adaptive / AI-assisted control (future)
