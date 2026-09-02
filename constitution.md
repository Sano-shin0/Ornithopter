# ORNITHOPTER — Project Constitution

**Version:** 1.0
**Status:** Active
**Project:** ORNITHOPTER
**Domain:** Bio-inspired flapping-wing aircraft / Ornithopter engineering

---

# 1. Purpose

ORNITHOPTER is an engineering project dedicated to the research, design, simulation, construction, testing, and validation of a bio-inspired flapping-wing aircraft.

The project may involve multiple engineering disciplines, including:

* aerodynamics;
* flight mechanics;
* structures;
* mechanical design;
* mechanisms;
* materials;
* propulsion;
* electronics;
* embedded systems;
* control systems;
* software;
* manufacturing;
* experimentation.

The repository is the single source of truth for the project's documented engineering knowledge, decisions, calculations, designs, simulations, tests, and validation status.

---

# 2. Engineering Philosophy

The project follows a traceable engineering process:

**Requirement → Research → Assumption → Model → Calculation → Design → Simulation → Prototype → Test → Validation**

No important engineering decision should be made without sufficient justification.

The project must distinguish clearly between:

* known facts;
* assumptions;
* theoretical predictions;
* simulation results;
* experimental measurements;
* engineering judgments.

These categories must never be presented as equivalent.

---

# 3. Scientific Integrity

## 3.1 No invented information

No agent, contributor, or document may invent:

* experimental results;
* physical constants;
* material properties;
* manufacturer specifications;
* scientific references;
* simulation results;
* measurements;
* test results.

If information is unknown, it must be explicitly identified as unknown or estimated.

---

## 3.2 Sources

Important external information must be traceable to its source.

Sources should preferably be:

1. peer-reviewed scientific literature;
2. recognized engineering textbooks;
3. official standards;
4. manufacturer documentation;
5. official technical documentation;
6. reputable technical publications;
7. other sources when necessary, with their limitations clearly identified.

When a source is uncertain, outdated, secondary, or potentially unreliable, this must be stated.

---

## 3.3 Reproducibility

Important calculations and simulations should be reproducible whenever practical.

A calculation should contain enough information to determine:

* input parameters;
* assumptions;
* equations;
* units;
* intermediate steps when relevant;
* output;
* interpretation.

---

# 4. Units and Quantities

The International System of Units (SI) is the default system.

Preferred units include:

* mass: kg
* length: m
* time: s
* force: N
* torque: N·m
* energy: J
* power: W
* pressure: Pa
* velocity: m/s
* angular velocity: rad/s
* frequency: Hz
* temperature: K

Non-SI units may be used when required by an external source, component datasheet, manufacturing process, or standard, but conversions must be made explicit when used in engineering calculations.

Every important numerical quantity must have an associated unit.

---

# 5. Assumptions

Every significant engineering model must explicitly identify its assumptions.

Examples include:

* incompressible flow;
* steady flow;
* inviscid flow;
* rigid body assumption;
* linear elasticity;
* small-angle approximation;
* negligible mass;
* constant temperature;
* ideal actuator;
* ideal sensor.

An assumption must never silently become a fact.

When an assumption has a significant influence on the result, its validity must be discussed.

---

# 6. Requirements

Requirements define what the system must accomplish.

Requirements must be:

* identifiable;
* measurable whenever possible;
* testable;
* traceable;
* independent from implementation details whenever possible.

A requirement should describe **what the system must achieve**, not prematurely dictate how it must achieve it.

Example:

Good:

> The aircraft shall maintain controlled flight for at least X minutes.

Bad:

> The aircraft shall use motor Y to maintain flight for X minutes.

The second statement is a design decision rather than a pure requirement.

---

# 7. Traceability

Important engineering elements should be traceable through the development chain:

**Requirement → Specification → Research → Calculation/Model → Design Decision → Implementation → Test → Validation**

When practical, documents should reference the requirement or decision they support.

This allows the project to answer:

* Why was this component selected?
* Which requirement does this design satisfy?
* Which calculation justified this dimension?
* Which test validated this assumption?
* Which evidence supports this claim?

---

# 8. Engineering Decisions

Significant design decisions must be documented.

Examples:

* material selection;
* actuator selection;
* battery selection;
* wing geometry;
* flapping mechanism;
* control architecture;
* sensor selection;
* structural architecture;
* manufacturing method.

Important decisions should document:

1. Problem;
2. Requirements;
3. Options considered;
4. Evaluation criteria;
5. Analysis;
6. Selected solution;
7. Reason for selection;
8. Consequences;
9. Remaining uncertainties.

The project must avoid undocumented decisions that become impossible to justify later.

---

# 9. Mass and Energy Accounting

Mass and energy are first-class engineering constraints.

The project should maintain traceability of:

* component mass;
* total aircraft mass;
* center of gravity;
* power consumption;
* energy capacity;
* estimated endurance;
* actuator requirements.

Whenever possible, mass and power budgets should be updated when major design decisions change.

---

# 10. Simulation

Simulation is a development and prediction tool.

A successful simulation does not automatically constitute experimental validation.

Simulation documentation should identify:

* model;
* assumptions;
* parameters;
* boundary conditions;
* solver/tool;
* mesh or discretization when relevant;
* convergence criteria when relevant;
* results;
* limitations.

Simulation results must not be presented as measured physical performance.

---

# 11. Experimental Testing

Experimental testing is required to validate important physical assumptions and predictions.

Tests should define, when applicable:

* objective;
* setup;
* equipment;
* procedure;
* measured quantities;
* environmental conditions;
* uncertainties;
* acceptance criteria;
* results;
* conclusions.

Raw experimental data should be preserved whenever practical.

Measurements must not be altered to make results appear better.

---

# 12. Validation Levels

The project uses the following conceptual validation hierarchy:

### Level 0 — Hypothesis

An unverified assumption or proposed idea.

### Level 1 — Analytical

Supported by mathematical or physical analysis.

### Level 2 — Numerical

Supported by simulation or computational modelling.

### Level 3 — Component Test

Verified experimentally at component level.

### Level 4 — Subsystem Test

Verified experimentally at subsystem level.

### Level 5 — System Test

Verified experimentally as an integrated aircraft system.

### Level 6 — Flight Validation

Validated through controlled flight testing.

A claim must not be described as experimentally validated if it has only reached an analytical or simulation level.

---

# 13. Safety

Safety takes priority over performance.

The project must consider risks associated with:

* moving wings;
* rotating mechanisms;
* actuators;
* batteries;
* electrical systems;
* structural failure;
* uncontrolled flight;
* high-speed components;
* testing environments.

A design must not be tested at a higher-risk level without appropriate safeguards.

---

# 14. AI Agent Rules

AI agents are assistants, not authorities.

An AI agent must:

1. distinguish facts from assumptions;
2. identify uncertainty;
3. avoid inventing information;
4. cite important external sources;
5. verify units;
6. check dimensional consistency when applicable;
7. identify missing information;
8. ask for clarification when requirements are ambiguous;
9. preserve existing requirements;
10. never silently modify important engineering decisions;
11. explain significant calculations;
12. identify limitations of models and simulations;
13. avoid claiming experimental validation without experimental evidence.

When an AI agent disagrees with an existing design decision, it should explain the disagreement and propose a documented engineering review rather than silently changing the design.

---

# 15. Human Authority

The final engineering decision belongs to the project owner.

AI-generated calculations, designs, recommendations, and research must be reviewed before being treated as authoritative engineering information.

The AI system must never represent an unverified proposal as an approved project decision.

---

# 16. Repository Organization

The repository follows these conceptual responsibilities:

* `specs/` — system and subsystem specifications;
* `research/` — research and technical knowledge;
* `engineering/` — calculations, models, sizing, and engineering studies;
* `cad/` — computer-aided design;
* `simulations/` — numerical simulations;
* `electronics/` — electronic hardware;
* `firmware/` — embedded software;
* `software/` — external software and analysis tools;
* `manufacturing/` — fabrication and assembly information;
* `testing/` — experimental testing and results;
* `prototypes/` — physical prototype history;
* `documentation/` — human-oriented project documentation;
* `.ai/` — AI agents, workflows, rules, and templates;
* `archive/` — obsolete but historically relevant material.

Files should be stored in the directory corresponding to their primary purpose.

---

# 17. Version Control

Git is used to preserve project history.

Important changes should have meaningful commit messages.

Examples:

* `Add initial aerodynamic requirements`
* `Update wing sizing calculation`
* `Add P001 structural test results`
* `Revise flapping mechanism design`

Large changes should not be hidden inside vague commits such as:

* `stuff`
* `update`
* `fix`
* `changes`

when a more descriptive message is possible.

---

# 18. Change Management

When an important requirement changes, dependent calculations, designs, simulations, and tests should be reviewed.

A change to one subsystem must be considered for possible effects on:

* mass;
* center of gravity;
* power;
* aerodynamics;
* structure;
* control;
* manufacturing;
* safety;
* other subsystems.

---

# 19. Uncertainty

Engineering results should be presented with appropriate awareness of uncertainty.

When an important quantity is estimated, the document should identify it as an estimate.

When uncertainty can reasonably be quantified, it should be reported.

False precision must be avoided.

For example:

Prefer:

> Estimated mass: approximately 420 g.

over:

> Mass = 0.420000 kg

when the underlying uncertainty is much larger.

---

# 20. Design Maturity

A design should progressively move through:

**Concept → Preliminary Design → Detailed Design → Prototype → Tested Prototype → Validated System**

The project must clearly identify the maturity of important designs.

A CAD model must not automatically be interpreted as a manufacturable or validated design.

---

# 21. Documentation Language

The primary project language is English for technical documentation, code, variable names, filenames, and engineering terminology.

French may be used for discussion and explanations outside the technical repository when useful.

Technical documents should remain clear, concise, and unambiguous.

---

# 22. Constitution Amendments

This constitution may evolve as the project develops.

Changes to fundamental rules should:

1. be explicitly documented;
2. have a clear reason;
3. preserve project traceability;
4. use version control.

The constitution must not be modified merely to make an inconvenient result appear acceptable.

---

# 23. Core Principle

The project follows one fundamental principle:

> **No important engineering claim without traceable evidence, explicit assumptions, and an appropriate level of validation.**

The objective is not simply to make an aircraft that flies.

The objective is to understand, design, build, measure, and progressively validate an engineering system whose behavior can be explained and reproduced.

