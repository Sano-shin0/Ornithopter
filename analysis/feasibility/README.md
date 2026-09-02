# ORNITHOPTER Feasibility Study

**Status:** DRAFT
**Revision:** 0.1
**Mission Reference:** `specs/system/mission.md`
**Requirements Reference:** `specs/system/requirements.md`

---

## 1. Purpose

The purpose of this study is to determine whether the proposed ORNITHOPTER robotic bird is physically and technically feasible before detailed subsystem design begins.

The study shall determine whether the system can realistically achieve controlled flapping-wing flight within the intended approximate scale.

---

## 2. Primary Questions

The feasibility study shall answer:

1. Can the wings generate sufficient aerodynamic force?
2. Can the mechanism produce the required wing motion?
3. Can the actuator provide sufficient torque and power?
4. Can the energy system provide the required energy?
5. Can the resulting total mass remain compatible with flight?
6. Can the system achieve the preliminary target flight speed?
7. Can the system potentially achieve the preliminary endurance target?
8. What parameters are the dominant limitations?
9. Which assumptions require experimental validation?

---

## 3. Analysis Chain

The analysis shall follow:

```text
Mission
   ↓
Mass Estimate
   ↓
Wing Geometry
   ↓
Aerodynamic Forces
   ↓
Required Thrust / Lift
   ↓
Mechanical Requirements
   ↓
Actuator Requirements
   ↓
Electrical Power
   ↓
Battery Requirements
   ↓
Total Mass
   ↓
Iteration
```

The calculations shall be iterative.

A preliminary result shall not be considered final until the interaction between mass, aerodynamics, propulsion, and energy has been evaluated.

---

## 4. Engineering Philosophy

The feasibility study shall avoid premature selection of components.

The following shall not be selected solely from intuition:

* motor,
* battery,
* wing dimensions,
* flapping frequency,
* mechanism,
* materials.

Instead, requirements shall first be derived from physical analysis.

---

## 5. Assumptions

Every important assumption shall be explicitly documented.

Each assumption shall include:

* identifier,
* value,
* unit,
* source,
* confidence,
* justification,
* and sensitivity where appropriate.

Example:

```text
ASSUMP-AERO-001
Parameter: Air density
Value: 1.225 kg/m³
Condition: Standard sea-level atmosphere
Confidence: High
```

---

## 6. Parameter Status

Parameters shall be classified as:

* **Known** — directly specified by the project
* **Measured** — obtained experimentally
* **Literature** — obtained from external research
* **Estimated** — engineering estimate
* **Assumed** — temporary assumption
* **Derived** — calculated from other parameters
* **Unknown** — currently unresolved

---

## 7. Validation Philosophy

A theoretical calculation is not automatically considered validated.

Important predictions shall progressively be compared with:

* analytical models,
* numerical simulations,
* laboratory measurements,
* prototype testing,
* and flight testing.

---

## 8. Expected Output

The feasibility study shall produce:

* preliminary mass range,
* preliminary wing dimensions,
* aerodynamic force estimates,
* flapping requirements,
* mechanical power estimate,
* electrical power estimate,
* battery requirement,
* sensitivity analysis,
* major technical risks,
* and a feasibility conclusion.

---

## 9. Feasibility Classification

The project shall use:

### FEASIBLE

Available evidence indicates that the requirement can realistically be achieved.

### CONDITIONALLY FEASIBLE

The requirement appears achievable but depends on unresolved parameters or experimental validation.

### CURRENTLY INFEASIBLE

Available evidence indicates that the requirement cannot currently be achieved under the defined constraints.

### UNKNOWN

Insufficient information exists to make a reliable conclusion.

---

## 10. Iteration

The feasibility study shall be continuously updated as new information becomes available.

A change in one major parameter may require recalculation of:

* mass,
* lift,
* thrust,
* power,
* energy,
* and endurance.

---

## 11. Current Status

The ORNITHOPTER feasibility study is currently in its initial analytical phase.

No final hardware architecture has been selected.
