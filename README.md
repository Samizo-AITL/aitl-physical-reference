# aitl-physical-reference

This repository provides a **physical reference PCB**
that anchors abstract control and logic concepts
into **real voltage, current, and copper**.

It is intentionally minimal and generic, focusing on
**observability, physical constraints, and manufacturability**.

---

## Purpose

- Fix abstract logic into real **V–I behavior**
- Provide a **measurable and visible physical endpoint**
- Serve as a reusable **physical reference**, not a framework

This board is designed to be used *by* higher-level architectures
(e.g. control logic, supervisory systems),
but does **not depend on them**.

---

## What This Is

- A minimal PCB with:
  - LED (observable output)
  - Resistor (physical constraint)
  - Switch (event input)
  - Test point (measurement)
  - Defined board outline (Edge.Cuts)

- A reference for:
  - Physical constraints
  - Boundary definition
  - Logic-to-hardware grounding

---

## What This Is NOT

- Not a full controller
- Not MCU-centric
- Not optimized for performance
- Not tied to any single architecture or framework

---

## Architecture Mapping (Conceptual)

| Conceptual Role | Physical Element |
|-----------------|------------------|
| Output state    | LED              |
| Constraint      | Resistor         |
| Event           | Switch           |
| Observation     | Test point       |
| Boundary        | PCB outline      |

---

## Toolchain

- **CAD**: KiCad
- **Focus**: Single-layer / simple routing
- **Output**: Manufacturable Gerber data

---

## Usage

This board can be used as a **physical grounding reference**
in architectures such as:

- Control systems
- Supervisory logic
- Educational hardware
- Architecture-for-logic-to-physical mappings (e.g. AITL)

---

## Status

- v0: Minimal physical reference (LED / R / SW / TP)

---

## License

Open hardware friendly license.
