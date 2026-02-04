# aitl-physical-control

Minimal **physical control reference board (v3)** for AITL.  
This project adds **one controllable element** to the frozen physical loop defined in
`aitl-physical-reference`, without changing the loop topology.

---

## Purpose

- Provide a **minimal control insertion** into a fixed V–I loop
- Observe how **continuous control** affects current and voltage
- Keep the physical loop **non-branching and observable**

This board is **not** a controller, MCU platform, or application PCB.

---

## What This Board Is

- Single closed loop: `+5V → RV → R → LED → GND`
- One control element: **potentiometer (RV1)**
- Explicit observation points:
  - **TP1**: +5V
  - **TP2**: GND
- DRC clean, manufacturable

---

## What This Board Is Not

- No MCU
- No GPIO semantics
- No feedback control logic
- No timing or intelligence

Those belong to higher layers.

---

## Schematic Overview

- **RV1**: Trimmer potentiometer (used as 2-terminal variable resistor)
- **R1**: Current limiting resistor
- **D1**: LED (visual current indicator)
- **TP1**: +5V test point
- **TP2**: GND test point

---

## PCB Notes

- RV1 wiper is **physically shorted** to one terminal (intentional)
- Single-layer routing (F.Cu)
- No ground plane required
- Loop integrity preserved from v2

---

## Files

```
hardware/kicad/aitl-physical-control/
├─ aitl-physical-control.kicad_pro
├─ aitl-physical-control.kicad_sch
├─ aitl-physical-control.kicad_pcb
└─ fp-info-cache
```

---

## Usage

1. Supply +5V at TP1
2. Observe LED brightness
3. Rotate RV1 to vary current
4. Measure voltage/current at TP1 / TP2

---

## Position in AITL Hardware Stack

- `aitl-physical-reference` : frozen physical loop (v2)
- **`aitl-physical-control` : minimal control insertion (v3)**
- Higher layers (FSM / PID / MCU) build on top of this

---

## Status

- v3 complete
- No further revisions planned
- Changes should be introduced as **experiments**, not new versions
