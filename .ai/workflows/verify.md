# Verification Workflow

## Purpose

Independently challenge an engineering claim, calculation, design, simulation, or implementation.

The objective is to find errors, inconsistencies, unsupported assumptions, and missing evidence.

---

## Input

Any important:

* requirement;
* calculation;
* design decision;
* simulation result;
* implementation;
* test result;
* engineering claim.

---

## Process

### Step 1 — Identify the claim

State exactly what is being verified.

---

### Step 2 — Identify the acceptance criteria

Determine what constitutes a successful result.

---

### Step 3 — Check traceability

Determine whether the claim can be traced to:

* requirement;
* source;
* calculation;
* model;
* measurement;
* test.

---

### Step 4 — Check assumptions

Challenge:

* physical assumptions;
* boundary conditions;
* simplifications;
* estimated parameters;
* unknowns.

---

### Step 5 — Check units

Verify dimensional consistency and unit conversions.

---

### Step 6 — Check calculations

Where practical:

* independently reproduce calculations;
* use alternative formulations;
* perform order-of-magnitude checks;
* test limiting cases.

---

### Step 7 — Check physical plausibility

Ask whether the result is physically reasonable.

---

### Step 8 — Check interfaces

Determine whether another subsystem invalidates the conclusion.

---

### Step 9 — Check evidence level

Classify the result as:

* hypothesis;
* analytical;
* numerical;
* component-tested;
* subsystem-tested;
* system-tested;
* flight-validated.

---

### Step 10 — Report

Classify the result as:

### PASS

Sufficient evidence supports the claim.

### CONDITIONAL

The claim appears plausible but requires additional evidence.

### FAIL

The claim is unsupported, inconsistent, or incorrect.

---

## Output

The verification report should contain:

* claim;
* acceptance criteria;
* evidence;
* checks performed;
* identified issues;
* severity;
* result;
* required corrections;
* recommended additional tests.

---

## Principle

The verification agent must attempt to disprove the claim rather than merely confirm it.

A result that survives serious attempts to invalidate it is more trustworthy than a result that was only checked superficially.
