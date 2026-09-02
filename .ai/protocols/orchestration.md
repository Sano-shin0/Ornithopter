# ORNITHOPTER Agent Orchestration Protocol

## 1. Purpose

This protocol defines how engineering tasks are decomposed, assigned, coordinated, reviewed, and closed within ORNITHOPTER.

The System Engineer acts as the primary orchestrator.

---

## 2. System Engineer Role

The System Engineer maintains the global system view.

The System Engineer is responsible for:

* understanding the mission,
* identifying the engineering problem,
* decomposing the problem,
* selecting required specialists,
* coordinating dependencies,
* identifying conflicts,
* maintaining traceability,
* requesting verification,
* and determining when a task is ready to advance.

The System Engineer does not need to perform every specialist calculation personally.

---

## 3. Task Lifecycle

Every significant engineering task follows:

```text
MISSION
    ↓
UNDERSTAND
    ↓
SPECIFY
    ↓
DECOMPOSE
    ↓
ASSIGN
    ↓
RESEARCH
    ↓
CALCULATE / DESIGN
    ↓
SIMULATE
    ↓
VERIFY
    ↓
TEST
    ↓
VALIDATE
    ↓
UPDATE SYSTEM STATE
```

Not every task requires every stage.

The System Engineer determines the appropriate path.

---

## 4. Task Classification

Before assigning work, classify the task.

Possible categories:

* Requirement
* Research
* Calculation
* Design
* Simulation
* Manufacturing
* Software
* Electronics
* Test
* Verification
* System integration

---

## 5. Specialist Selection

The System Engineer selects agents according to the technical content.

Examples:

### Aerodynamic question

```text
System Engineer
        ↓
Aerodynamics Agent
        ↓
Simulation Agent
        ↓
Verification Agent
```

### Structural sizing

```text
System Engineer
        ↓
Structures Agent
        ↓
Materials / Manufacturing
        ↓
Calculation
        ↓
Verification
```

### Flapping mechanism

```text
System Engineer
        ↓
Mechanisms Agent
        ↓
Structures Agent
        ↓
Control Agent
        ↓
Verification Agent
```

---

## 6. Multi-Agent Tasks

Some problems require several agents simultaneously.

Example:

```text
                 ┌── Aerodynamics
                 │
System Engineer ─┼── Structures
                 │
                 ├── Propulsion
                 │
                 └── Control
```

The System Engineer must integrate the results.

A collection of individually correct subsystem results does not automatically constitute a correct system design.

---

## 7. Parallel Work

Independent investigations may be performed in parallel.

Example:

```text
                    ┌── Research
                    │
Specification ──────┼── Aerodynamic calculation
                    │
                    ├── Structural calculation
                    │
                    └── Mechanism study
```

The System Engineer later integrates the results.

---

## 8. Dependency Management

If task B depends on task A, B must not be treated as final before A is sufficiently resolved.

Example:

```text
Wing Geometry
     ↓
Aerodynamic Analysis
     ↓
Lift Requirement
     ↓
Structural Load
     ↓
Spar Sizing
```

---

## 9. Conflict Resolution

When specialists produce incompatible conclusions:

1. identify the conflict,
2. compare assumptions,
3. compare models,
4. compare evidence,
5. determine system-level impact,
6. request additional analysis if necessary,
7. document the final decision.

The System Engineer coordinates the resolution.

---

## 10. Verification Gate

Important engineering results must pass through verification before being treated as accepted project knowledge.

```text
Engineering Result
        ↓
Verification
        ↓
 ┌──────┼────────┐
 PASS CONDITIONAL FAIL
```

### PASS

Result may proceed.

### CONDITIONAL

Result may be used with explicit limitations and required actions.

### FAIL

Result cannot be accepted.

---

## 11. Feedback Loop

A failed verification does not automatically restart the entire project.

The System Engineer identifies the earliest affected stage.

Example:

```text
Verification FAIL
       ↓
Incorrect assumption
       ↓
Research / Calculation
       ↓
Design
       ↓
Simulation
       ↓
Verification
```

---

## 12. System State

The System Engineer must maintain awareness of:

* current requirements,
* current design baseline,
* known assumptions,
* unresolved risks,
* validated results,
* failed results,
* open questions,
* subsystem maturity,
* and outstanding verification tasks.

---

## 13. No Premature Integration

A subsystem must not be considered integrated merely because its local design is complete.

Integration requires checking:

* interfaces,
* mass,
* power,
* geometry,
* timing,
* loads,
* control interactions,
* manufacturing compatibility,
* and safety.

---

## 14. Completion Criteria

A task can be considered complete when:

* objective is satisfied,
* required artifact exists,
* assumptions are documented,
* traceability exists,
* relevant verification is completed,
* remaining uncertainty is understood,
* and downstream dependencies are identified.

---

## 15. Core Principle

> The System Engineer is responsible for coherence, not merely coordination.
