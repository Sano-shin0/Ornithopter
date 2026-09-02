# Calculation Rules

## 1. Purpose

These rules govern all engineering calculations performed for ORNITHOPTER.

---

## 2. Calculation Structure

Every significant calculation must contain:

1. Objective
2. Inputs
3. Sources
4. Assumptions
5. Model
6. Equations
7. Calculation
8. Result
9. Units
10. Sanity check
11. Uncertainty
12. Limitations
13. Next action

---

## 3. Inputs

Every important input must include:

* symbol,
* numerical value,
* unit,
* source,
* uncertainty when available.

Example:

```text
ρ = 1.225 kg/m³
Source: standard atmospheric condition
Condition: sea level, approximately 15 °C
```

---

## 4. Equations

Equations must be presented clearly.

Whenever an equation is not fundamental or universally established, provide its source.

If an approximation is used, state it explicitly.

---

## 5. Dimensional Analysis

Calculations involving physical quantities must be dimensionally checked.

If units do not match, stop the calculation and resolve the inconsistency.

---

## 6. Numerical Precision

Do not create artificial precision.

The number of reported significant digits should reflect:

* input accuracy,
* model accuracy,
* measurement uncertainty,
* and numerical uncertainty.

---

## 7. Sanity Checks

Significant calculations should include at least one independent sanity check.

Possible methods:

* order-of-magnitude estimate,
* limiting case,
* alternate equation,
* comparison with literature,
* comparison with experimental data,
* conservation law,
* dimensional analysis.

---

## 8. Sensitivity

When appropriate, determine which parameters dominate the result.

Example:

If:

```text
P ∝ m³
```

then uncertainty in mass has a much larger effect than a parameter appearing linearly.

Important sensitivities should be documented.

---

## 9. Numerical Tools

Code, spreadsheets, symbolic mathematics, or numerical software may be used.

However:

> Software output is not automatically a verified engineering result.

The governing model and assumptions must remain understandable independently of the software.

---

## 10. Reproducibility

A calculation should be reproducible by another engineer.

Record:

* input values,
* equations,
* method,
* software/tool when relevant,
* relevant parameters,
* and calculation procedure.

---

## 11. Changed Inputs

If an upstream value changes, dependent calculations must be identified.

Do not silently reuse outdated values.

---

## 12. Result Classification

Each result should be identifiable as one of:

* theoretical,
* estimated,
* calculated,
* simulated,
* measured,
* validated.

---

## 13. Independent Verification

Critical calculations should be reviewed independently.

The Verification Agent should attempt to reproduce or challenge the calculation.

---

## 14. Forbidden Behavior

Never:

* hide calculation steps when they matter,
* omit units,
* silently substitute values,
* use unexplained constants,
* mix incompatible unit systems,
* or claim greater accuracy than justified.
