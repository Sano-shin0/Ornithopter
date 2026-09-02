# Specify Workflow

## Purpose

Transform an initial idea, request, problem, or engineering objective into a clear and testable engineering specification.

---

## Input

The input may be:

* a vague idea;
* an engineering problem;
* a user request;
* a performance objective;
* a design limitation;
* an observed failure;
* a new project requirement.

The input does not need to be technically complete.

---

## Process

### Step 1 — Understand the objective

Determine what the user or project is actually trying to accomplish.

Do not immediately propose a solution.

---

### Step 2 — Identify the system

Determine which part of ORNITHOPTER is affected.

Possible systems include:

* aircraft;
* wing;
* flapping mechanism;
* structure;
* propulsion;
* electronics;
* power system;
* sensors;
* flight control;
* firmware;
* software.

---

### Step 3 — Identify requirements

Find existing relevant requirements in:

* `requirements.md`;
* relevant `specs/`;
* `constitution.md`.

Do not invent numerical requirements without explicit justification.

---

### Step 4 — Identify constraints

Identify:

* mass constraints;
* geometric constraints;
* power constraints;
* material constraints;
* manufacturing constraints;
* environmental constraints;
* safety constraints;
* budget constraints;
* available components;
* interfaces with other subsystems.

---

### Step 5 — Identify unknowns

Create an explicit list of information that is missing.

Classify each item as:

* required immediately;
* useful but non-critical;
* can be estimated;
* requires research;
* requires measurement;
* requires testing.

---

### Step 6 — Identify affected disciplines

Determine which specialist agents should participate.

Examples:

Aerodynamics
Structures
Mechanisms
Propulsion
Electronics
Control
Software
Simulation
Manufacturing
Verification

---

### Step 7 — Define acceptance criteria

Determine how success will be evaluated.

Acceptance criteria should be measurable whenever possible.

---

### Step 8 — Produce the specification

Create or update the appropriate file under:

`specs/`

The specification should contain:

* objective;
* scope;
* requirements;
* constraints;
* interfaces;
* assumptions;
* unknowns;
* acceptance criteria;
* dependencies;
* affected disciplines.

---

## Rules

Never:

* jump directly to implementation;
* invent missing requirements;
* silently modify existing requirements;
* hide uncertainty;
* prescribe a solution before understanding the problem.

The goal of this workflow is to define **what must be achieved**, not yet **how it will be achieved**.

---

## Output

A complete engineering specification that is:

* clear;
* measurable where possible;
* testable;
* traceable;
* independent from unnecessary implementation decisions.
