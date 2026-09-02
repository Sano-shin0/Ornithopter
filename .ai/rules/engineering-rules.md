# Engineering Rules

## 1. Purpose

These rules define the general engineering behavior expected from every agent working on the ORNITHOPTER project.

They apply to all disciplines, including aerodynamics, structures, mechanisms, propulsion, electronics, control, software, simulation, manufacturing, testing, and verification.

---

## 2. Engineering Integrity

Every engineering claim must be supported by one or more of:

* a documented source,
* an explicit assumption,
* an analytical calculation,
* a numerical simulation,
* experimental data,
* or an established physical law.

Agents must never present an assumption as a fact.

Agents must never invent:

* measurements,
* material properties,
* component specifications,
* experimental results,
* simulation results,
* references,
* standards,
* equations,
* manufacturer data,
* or design constraints.

If information is unavailable, explicitly state:

> Information unavailable.

or

> Assumption required.

---

## 3. Requirement Discipline

Agents must distinguish between:

* requirement,
* constraint,
* assumption,
* design choice,
* calculated result,
* measured result,
* and recommendation.

Requirements must not be silently modified.

If a requirement appears contradictory, unrealistic, incomplete, or physically impossible, the agent must flag it and request clarification or propose alternatives.

Agents must not transform a design preference into a mandatory requirement without justification.

---

## 4. Traceability

Important engineering decisions must remain traceable through the following chain:

Requirement
→ Specification
→ Research
→ Model
→ Calculation
→ Design Decision
→ Implementation
→ Test
→ Validation

When possible, documents should reference the relevant upstream and downstream artifacts.

---

## 5. Assumptions

Every non-obvious assumption must be explicitly documented.

Each important assumption should include:

* identifier,
* description,
* justification,
* expected impact,
* validity range if known,
* and how it could eventually be verified.

Example:

```text
ASSUMPTION-AERO-001

Description:
The flow is assumed incompressible.

Justification:
Expected Mach number remains sufficiently low.

Impact:
Density is treated as constant.

Verification:
Check Mach number during aerodynamic analysis.
```

---

## 6. Units

The SI system must be used by default.

All numerical quantities must include units unless they are explicitly dimensionless.

Agents must perform dimensional checks whenever calculations involve multiple physical quantities.

Conversions must be explicit.

Never mix:

* mm and m,
* g and kg,
* rpm and rad/s,
* degrees and radians,
* Pa and bar,
* N and kgf,

without explicitly converting them.

---

## 7. Physical Plausibility

Every significant result must be checked for physical plausibility.

At minimum, consider:

* order of magnitude,
* limiting cases,
* conservation laws,
* dimensional consistency,
* expected physical behavior,
* comparison with known reference values.

A mathematically correct result is not automatically an engineering-valid result.

---

## 8. Coupling Between Disciplines

Agents must identify cross-disciplinary dependencies.

Examples:

Aerodynamics ↔ Structures
Aerodynamics ↔ Propulsion
Mechanism ↔ Structures
Mechanism ↔ Control
Electronics ↔ Power
Power ↔ Mass
Mass ↔ Aerodynamics
Control ↔ Dynamics
Manufacturing ↔ Structures

A specialist must not optimize its subsystem while ignoring system-level consequences.

---

## 9. Mass and Energy

Mass and energy budgets are first-class engineering constraints.

Whenever applicable, agents must track:

* component mass,
* subsystem mass,
* total mass,
* center of gravity,
* power consumption,
* available power,
* energy storage,
* efficiency,
* losses,
* thermal consequences.

Any significant change in mass or power consumption must trigger consideration of its system-level consequences.

---

## 10. Uncertainty

Results must distinguish between:

* known values,
* estimated values,
* measured values,
* calculated values,
* assumed values,
* uncertain values.

When uncertainty is significant, quantify it when possible.

Avoid false precision.

Do not report:

```text
12.483729 N
```

if the underlying inputs only justify approximately:

```text
12.5 N
```

---

## 11. Engineering Maturity

The maturity of an engineering claim must be clear.

Use the following validation levels:

### Level 0 — Hypothesis

Conceptual expectation with no supporting analysis.

### Level 1 — Analytical

Supported by equations or analytical reasoning.

### Level 2 — Numerical

Supported by simulation or numerical analysis.

### Level 3 — Component Test

Verified experimentally on an individual component.

### Level 4 — Subsystem Test

Verified experimentally at subsystem level.

### Level 5 — System Test

Verified experimentally at complete-system level.

### Level 6 — Flight Validation

Validated under representative flight conditions.

Agents must never claim a higher validation level than the available evidence supports.

---

## 12. Safety

Safety-critical questions must be explicitly identified.

Examples include:

* structural failure,
* battery failure,
* high-speed rotating components,
* propulsive or flapping mechanisms,
* electrical hazards,
* thermal hazards,
* autonomous operation,
* loss of control,
* unexpected flight behavior.

Safety considerations must not be omitted merely because they are outside the immediate task.

---

## 13. Missing Information

When information required for a reliable conclusion is missing, the agent must:

1. identify the missing information,
2. explain why it matters,
3. estimate whether the conclusion can still proceed,
4. propose how to obtain it.

Do not silently invent the missing value.

---

## 14. Conflicting Results

When two calculations, simulations, sources, or experiments disagree:

* do not select the preferred result without analysis,
* identify the disagreement,
* identify possible causes,
* compare assumptions,
* compare models,
* compare input data,
* determine what additional evidence is required.

---

## 15. System-Level Priority

When subsystem optimization conflicts with system-level requirements, the System Engineer has authority to coordinate the resolution.

Specialist agents must expose the conflict rather than silently choosing one side.

---

## 16. Verification Independence

The Verification Agent must remain independent from the agent responsible for producing the result.

The objective of verification is to challenge the claim, not to justify it.

---

## 17. Forbidden Behavior

Agents must not:

* fabricate data,
* fabricate sources,
* hide uncertainty,
* silently change requirements,
* silently change assumptions,
* silently change design decisions,
* claim simulation equals validation,
* claim calculation equals experimental verification,
* ignore unit inconsistencies,
* ignore contradictory evidence,
* or present guesses as established facts.

---

## 18. Core Rule

> No important engineering claim without traceable evidence, explicit assumptions, and an appropriate level of validation.
