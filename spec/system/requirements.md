# ORNITHOPTER System Requirements

**ID:** REQ-SYS-DOC-001
**Title:** ORNITHOPTER System Requirements
**Status:** DRAFT
**Date:** 2026-09-02
**Owner:** System Engineer
**Mission Reference:** MISSION-SYS-001
**Revision:** 0.1

---

# 1. Purpose

This document translates the ORNITHOPTER mission into measurable and traceable system-level requirements.

Requirements define what the system shall accomplish.

They do not prescribe a specific implementation unless explicitly stated.

Design choices such as:

* motor type,
* actuator type,
* wing mechanism,
* material,
* battery technology,
* control algorithm,
* wing geometry,
* and manufacturing process

shall be determined through subsequent engineering analysis.

---

# 2. Requirement Classification

Requirements are classified into the following categories:

* **MUST** — fundamental requirement
* **SHOULD** — important target
* **TARGET** — desirable performance objective
* **FUTURE** — intended for a later development stage

---

# 3. System-Level Requirements

## REQ-SYS-001 — Flapping-Wing Flight

**Priority:** MUST
**Category:** Flight

ORNITHOPTER shall use controlled wing flapping as a primary mechanism for generating the aerodynamic forces required for flight.

**Verification:** Inspection + Test

---

## REQ-SYS-002 — Controlled Flight

**Priority:** MUST
**Category:** Flight Control

ORNITHOPTER shall be capable of maintaining controlled flight without requiring continuous direct stabilization by a human operator.

**Verification:** Flight Test

---

## REQ-SYS-003 — Flight Stability

**Priority:** MUST
**Category:** Flight Dynamics

ORNITHOPTER shall possess sufficient inherent and/or actively controlled stability to prevent uncontrolled divergence during the intended flight regime.

**Verification:** Analysis + Flight Test

---

## REQ-SYS-004 — Forward Flight

**Priority:** MUST
**Category:** Flight

ORNITHOPTER shall be capable of sustained forward flight.

**Preliminary Target Speed:** ≥ 20 km/h

**Verification:** Flight Test

**Status:** Preliminary

---

## REQ-SYS-005 — Gliding

**Priority:** MUST
**Category:** Flight

ORNITHOPTER shall be capable of entering and maintaining a gliding flight state in which sustained wing flapping is reduced or stopped while aerodynamic forces remain sufficient to maintain controlled descent or flight.

**Verification:** Flight Test

---

## REQ-SYS-006 — Glide Energy Reduction

**Priority:** SHOULD
**Category:** Energy

ORNITHOPTER shall use gliding when appropriate to reduce energy consumption during flight.

The optimal transition strategy shall be determined through aerodynamic and energy analysis.

**Verification:** Analysis + Flight Test

---

## REQ-SYS-007 — Takeoff Without Running

**Priority:** SHOULD
**Category:** Flight

The final ORNITHOPTER system should be capable of initiating flight without requiring a conventional runway or prolonged ground run.

Possible takeoff strategies include:

* jump-assisted takeoff,
* wing-assisted launch,
* elevated launch,
* or another biologically inspired mechanism.

**Verification:** Flight Test

---

## REQ-SYS-008 — Shoulder / Elevated Launch

**Priority:** FUTURE
**Category:** Operation

The mature system should be capable of initiating flight from an elevated position comparable to a human operator's shoulder or hand.

**Verification:** Demonstration

---

# 4. Performance Requirements

## REQ-PERF-001 — Minimum Flight Speed

**Priority:** TARGET

The system should achieve a minimum sustained forward flight speed of approximately:

**20 km/h**

The final requirement shall be established after aerodynamic analysis.

**Verification:** Flight Test

---

## REQ-PERF-002 — Flight Endurance

**Priority:** TARGET

The mature system should target a minimum flight endurance of:

**30 minutes**

The final endurance requirement shall be determined after:

* mass estimation,
* aerodynamic analysis,
* propulsion sizing,
* energy-budget analysis,
* and prototype testing.

**Verification:** Flight Test

**Status:** Preliminary

---

## REQ-PERF-003 — Mass

**Priority:** MUST

The total system mass shall remain sufficiently low to permit the required aerodynamic performance.

No fixed final mass limit is established at this stage.

Mass shall instead be determined through an iterative mass and performance budget.

**Verification:** Measurement + Analysis

---

## REQ-PERF-004 — Mass Budget

**Priority:** MUST

The project shall maintain a continuously updated mass budget covering:

* body,
* wings,
* mechanism,
* actuators,
* battery,
* electronics,
* sensors,
* wiring,
* structure,
* and payload.

**Verification:** Inspection

---

# 5. Physical Configuration Requirements

## REQ-GEO-001 — Bird-Like Configuration

**Priority:** MUST

The system shall use a configuration visually and mechanically inspired by a bird.

The system shall not be required to reproduce a specific bird species.

---

## REQ-GEO-002 — Preliminary Body Scale

**Priority:** TARGET

The initial design target for the body shall be approximately:

**30 cm characteristic body length**

The exact geometry shall be determined through engineering optimization.

**Verification:** Measurement

---

## REQ-GEO-003 — Wing Dimensions

**Priority:** TARGET

The initial design shall investigate wings with an approximate characteristic span of:

**30–35 cm per wing**

This value shall remain adjustable during aerodynamic optimization.

**Verification:** Measurement + Analysis

---

## REQ-GEO-004 — Wing Optimization

**Priority:** MUST

Wing geometry shall be selected based on a combination of:

* aerodynamic performance,
* mass,
* structural integrity,
* manufacturability,
* mechanism requirements,
* control authority,
* and energy efficiency.

The design shall not be constrained to a particular biological wing geometry.

**Verification:** Analysis

---

## REQ-GEO-005 — Wing Flexibility

**Priority:** SHOULD

The design shall investigate passive and/or active wing flexibility where it may improve:

* aerodynamic performance,
* energy efficiency,
* force generation,
* stability,
* or biological similarity.

**Verification:** Analysis + Test

---

## REQ-GEO-006 — Tail

**Priority:** TARGET

The system may incorporate a tail or other rear aerodynamic control surface if required for:

* stability,
* control,
* maneuverability,
* aerodynamic efficiency,
* or biological functionality.

A tail shall not be included solely for visual appearance if it introduces unnecessary mass or aerodynamic penalty.

**Verification:** Analysis + Test

---

# 6. Flapping Mechanism Requirements

## REQ-MECH-001 — Controlled Flapping

**Priority:** MUST

The wing flapping mechanism shall provide controlled and repeatable wing motion.

**Verification:** Test

---

## REQ-MECH-002 — Adjustable Flapping Parameters

**Priority:** SHOULD

The system should allow adjustment of relevant flapping parameters such as:

* frequency,
* amplitude,
* phase,
* and/or wing kinematics.

The exact controllable parameters shall depend on the selected mechanism.

**Verification:** Test

---

## REQ-MECH-003 — Mechanical Efficiency

**Priority:** MUST

The flapping mechanism shall be analyzed for:

* torque,
* power,
* mechanical losses,
* friction,
* backlash,
* vibration,
* and cyclic loading.

**Verification:** Analysis + Test

---

## REQ-MECH-004 — Cyclic Loading

**Priority:** MUST

The flapping mechanism and wing structure shall withstand repeated cyclic loading corresponding to the intended operating envelope.

**Verification:** Analysis + Fatigue Test

---

## REQ-MECH-005 — Mechanical Reliability

**Priority:** MUST

Critical mechanical components shall be evaluated for wear, fatigue, and failure modes.

**Verification:** Analysis + Test

---

# 7. Flight Control Requirements

## REQ-CTRL-001 — Attitude Stabilization

**Priority:** MUST

The system shall provide active and/or passive stabilization of:

* roll,
* pitch,
* and yaw.

**Verification:** Analysis + Flight Test

---

## REQ-CTRL-002 — Human Control

**Priority:** MUST

The initial flight prototype may be controlled by a human operator.

The control interface shall allow the operator to influence the intended flight state.

**Verification:** Demonstration

---

## REQ-CTRL-003 — Progressive Autonomy

**Priority:** FUTURE

The mature ORNITHOPTER system shall be capable of autonomous flight stabilization and navigation.

**Verification:** Flight Test

---

## REQ-CTRL-004 — Commanded Behavior

**Priority:** FUTURE

The mature system shall be capable of responding to defined high-level commands from its operator.

Potential commands may include:

* come,
* follow,
* land,
* return,
* take off,
* change direction,
* or other defined behaviors.

The exact command set shall be specified later.

**Verification:** Demonstration + Flight Test

---

## REQ-CTRL-005 — Autonomous Flight

**Priority:** FUTURE

The mature system shall be capable of maintaining controlled flight without continuous manual stabilization.

**Verification:** Flight Test

---

# 8. Interaction Requirements

## REQ-INT-001 — Operator Interaction

**Priority:** FUTURE

The system shall provide an operator interface through which the user can issue flight commands.

The final interface may include:

* remote control,
* mobile device,
* dedicated controller,
* voice command,
* acoustic signal,
* gesture,
* or another interface.

The final implementation shall be selected during the control-system design phase.

---

## REQ-INT-002 — Recall Behavior

**Priority:** FUTURE

The mature system should be capable of responding to a defined recall command from its operator.

A whistle or other acoustic signal may be investigated as a recall mechanism.

This requirement shall remain subject to:

* acoustic environment,
* sensor capability,
* recognition reliability,
* safety,
* and false-trigger analysis.

---

## REQ-INT-003 — Perching

**Priority:** FUTURE

The mature system should investigate the ability to land or perch on a suitable elevated surface such as:

* the operator's hand,
* shoulder,
* branch-like structure,
* or dedicated perch.

**Verification:** Demonstration

---

# 9. Environmental Requirements

## REQ-ENV-001 — Initial Operating Environment

**Priority:** MUST

Initial flight testing shall be performed in sufficiently open environments where obstacles and environmental complexity can be controlled.

Initial development shall not require operation inside:

* dense forests,
* highly obstructed environments,
* or severe weather.

---

## REQ-ENV-002 — Progressive Environmental Capability

**Priority:** FUTURE

Environmental capability shall progressively expand to include more challenging conditions such as:

* wind,
* turbulence,
* reduced visibility,
* vegetation,
* and other obstacles.

---

## REQ-ENV-003 — Open-Sky Operation

**Priority:** MUST

The initial flight envelope shall assume open-sky operation with sufficient clearance from obstacles.

---

# 10. Energy Requirements

## REQ-ENERGY-001 — Energy Budget

**Priority:** MUST

The project shall maintain a system-level energy budget including:

* battery energy,
* actuator consumption,
* control electronics,
* sensors,
* communication,
* and auxiliary systems.

---

## REQ-ENERGY-002 — Energy-Efficient Flight

**Priority:** MUST

The flight architecture shall investigate energy-efficient operating modes including:

* gliding,
* reduced flapping,
* optimized flapping frequency,
* optimized wing kinematics,
* and other appropriate strategies.

---

## REQ-ENERGY-003 — Battery Sizing

**Priority:** MUST

Battery capacity shall be determined from the validated system power requirement and desired endurance rather than selected independently.

---

# 11. Instrumentation Requirements

## REQ-INS-001 — Flight Measurement

**Priority:** MUST

The system shall provide sufficient instrumentation to characterize its flight behavior.

Potential measurements include:

* position,
* acceleration,
* angular velocity,
* attitude,
* airspeed,
* electrical power,
* wing motion,
* and actuator state.

---

## REQ-INS-002 — Data Logging

**Priority:** MUST

Relevant flight and system data shall be recorded for post-flight analysis.

---

## REQ-INS-003 — Experimental Reproducibility

**Priority:** MUST

Testing shall be structured so that comparable experiments can be repeated under documented conditions.

---

# 12. Research Requirements

## REQ-RES-001 — Literature Integration

**Priority:** MUST

The project shall use relevant existing scientific and engineering research to inform the design.

Existing research shall be:

* identified,
* referenced,
* evaluated,
* and distinguished from original project results.

---

## REQ-RES-002 — Original Investigation

**Priority:** SHOULD

The project should investigate questions that remain insufficiently understood or experimentally characterized.

Any claimed original contribution shall be supported by appropriate evidence.

---

## REQ-RES-003 — Biological Inspiration

**Priority:** SHOULD

Biological flight mechanisms shall be investigated as potential sources of engineering solutions.

Biological mechanisms shall be evaluated quantitatively rather than adopted solely because they occur in nature.

---

# 13. Safety Requirements

## REQ-SAFE-001 — Controlled Testing

**Priority:** MUST

Flight testing shall be performed under controlled conditions appropriate to the current prototype capability.

---

## REQ-SAFE-002 — Mechanical Safety

**Priority:** MUST

The flapping mechanism shall be evaluated for hazards associated with:

* moving wings,
* high-speed components,
* mechanical failure,
* and stored mechanical energy.

---

## REQ-SAFE-003 — Electrical Safety

**Priority:** MUST

The electrical and energy-storage systems shall be evaluated for:

* overcurrent,
* overheating,
* short circuits,
* battery failure,
* and other relevant hazards.

---

## REQ-SAFE-004 — Loss of Control

**Priority:** MUST

The system shall have a defined response to loss of:

* communication,
* control authority,
* critical sensor information,
* or propulsion capability.

---

# 14. Development Requirements

## REQ-DEV-001 — Progressive Development

**Priority:** MUST

The system shall be developed progressively from component validation to integrated flight.

---

## REQ-DEV-002 — Prototype Capability

**Priority:** MUST

Early prototypes shall not be required to implement the complete final mission.

The minimum initial objective is controlled flight.

---

## REQ-DEV-003 — Future Biological Capabilities

**Priority:** FUTURE

Advanced capabilities such as:

* jumping,
* perching,
* autonomous recall,
* autonomous navigation,
* bird-like behaviors,
* and advanced environmental interaction

shall be introduced only after basic controlled flight has been demonstrated.

---

# 15. Requirement Traceability

The requirement hierarchy shall follow:

```text
MISSION
   │
   ├── Flight
   │    ├── Lift
   │    ├── Thrust
   │    ├── Stability
   │    └── Gliding
   │
   ├── Mechanism
   │    ├── Flapping
   │    ├── Efficiency
   │    └── Reliability
   │
   ├── Structure
   │    ├── Mass
   │    ├── Strength
   │    └── Fatigue
   │
   ├── Control
   │    ├── Stabilization
   │    ├── Manual Control
   │    └── Autonomy
   │
   ├── Energy
   │    ├── Battery
   │    ├── Power
   │    └── Endurance
   │
   ├── Interaction
   │    ├── Commands
   │    ├── Recall
   │    └── Perching
   │
   └── Validation
        ├── Measurement
        ├── Testing
        └── Flight Validation
```

---

# 16. Requirement Status

The following requirements contain preliminary or future targets and shall not be treated as final engineering specifications until validated.

| Requirement                        | Status      |
| ---------------------------------- | ----------- |
| REQ-PERF-001 — 20 km/h             | PRELIMINARY |
| REQ-PERF-002 — 30 min endurance    | PRELIMINARY |
| REQ-GEO-002 — ~30 cm body          | PRELIMINARY |
| REQ-GEO-003 — ~30–35 cm wings      | PRELIMINARY |
| REQ-CTRL-004 — High-level commands | FUTURE      |
| REQ-INT-002 — Whistle recall       | FUTURE      |
| REQ-INT-003 — Perching             | FUTURE      |
| REQ-CTRL-005 — Autonomous flight   | FUTURE      |

---

# 17. Open Engineering Questions

The following questions must be resolved through engineering work rather than arbitrary assumptions:

1. What wing area is required for the target mass?
2. What flapping frequency is optimal?
3. What stroke amplitude is optimal?
4. What wing kinematics generate the best lift-to-power ratio?
5. How flexible should the wings be?
6. What mechanism provides the best power-to-mass ratio?
7. What actuator provides sufficient torque and speed?
8. Can passive wing pitching improve efficiency?
9. Can energy be recovered during the flapping cycle?
10. How should roll, pitch, and yaw be controlled?
11. Is a tail required?
12. What mass distribution produces acceptable stability?
13. What battery technology provides sufficient specific energy?
14. What aerodynamic model is sufficiently accurate for preliminary design?
15. What experimental setup is required to validate the aerodynamic model?
16. What minimum power is required for sustained flight?
17. What flight mode provides the best endurance?
18. How should the system transition between flapping and gliding?
19. What sensing architecture is required for autonomous flight?
20. What biological mechanisms provide measurable engineering advantages?

---

# 18. Requirement Evolution

Requirements shall evolve as knowledge increases.

A requirement may be:

```text
PROPOSED
   ↓
PRELIMINARY
   ↓
ANALYZED
   ↓
VALIDATED
   ↓
BASELINE
```

Requirements shall not be changed merely to match an existing design.

If a requirement becomes physically unrealistic, the change shall be documented and justified.

---

# 19. Next Engineering Stage

The next engineering stage is to determine the fundamental feasibility of the system.

Priority analyses shall include:

1. Preliminary mass budget
2. Wing loading
3. Required lift
4. Required thrust
5. Flapping kinematics
6. Power requirement
7. Battery feasibility
8. Mechanism feasibility
9. Preliminary stability
10. Initial aerodynamic model

These analyses shall establish whether the proposed mission is physically achievable with the intended scale and architecture.

---

# 20. Requirement Baseline

**Current status:** DRAFT

No requirement in this document shall be considered permanently frozen until sufficient engineering evidence exists.

The first formal baseline shall be established after preliminary feasibility analysis.

---

# 21. Core Requirement Philosophy

> **ORNITHOPTER requirements shall describe what the robotic bird must accomplish, while leaving the engineering team free to discover the most effective biological, mechanical, aerodynamic, electrical, and computational means of achieving those objectives.**
