# Simulation Workflow

## Purpose

Use numerical simulation to predict system behavior, investigate design alternatives, and identify potential problems before physical testing.

---

## Input

A defined simulation problem with:

* objective;
* model;
* geometry or system representation;
* parameters;
* boundary conditions;
* required outputs.

---

## Process

### Step 1 — Define the question

State what the simulation must determine.

---

### Step 2 — Select the simulation method

Examples:

* analytical model;
* CFD;
* FEA;
* multibody dynamics;
* flight dynamics;
* control simulation;
* circuit simulation;
* system simulation.

---

### Step 3 — Define assumptions

Document model assumptions and simplifications.

---

### Step 4 — Define parameters

Record:

* geometry;
* material properties;
* environmental conditions;
* loads;
* boundary conditions;
* initial conditions.

---

### Step 5 — Verify the model

Check:

* units;
* geometry;
* boundary conditions;
* mesh/discretization;
* solver settings;
* convergence;
* numerical stability.

---

### Step 6 — Run the simulation

Record the configuration required to reproduce the simulation.

---

### Step 7 — Analyze results

Identify:

* expected behavior;
* unexpected behavior;
* sensitivities;
* numerical artifacts;
* limitations.

---

### Step 8 — Compare with analytical or experimental evidence

Whenever possible, compare simulation results with:

* analytical calculations;
* literature;
* experimental measurements;
* manufacturer data.

---

## Critical Rule

A simulation result is not automatically experimental validation.

A simulation may increase confidence in a design, but physical validation requires appropriate experimental evidence.

---

## Output

The simulation record must contain:

* objective;
* model;
* assumptions;
* parameters;
* setup;
* solver/tool;
* results;
* convergence information when relevant;
* interpretation;
* limitations;
* comparison;
* recommended next action.
