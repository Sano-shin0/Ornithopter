# ORNITHOPTER Engineering Review Protocol

## 1. Purpose

This protocol defines engineering review gates for ORNITHOPTER.

---

## 2. Review Principle

Review exists to identify errors before they propagate downstream.

A review is not merely an approval step.

---

## 3. Review Levels

### Review Level 1 — Completeness

Check:

* required sections exist,
* inputs are present,
* units are present,
* references exist,
* assumptions are documented.

### Review Level 2 — Technical Consistency

Check:

* equations,
* physical model,
* interfaces,
* assumptions,
* numerical consistency,
* physical plausibility.

### Review Level 3 — Independent Verification

Attempt to independently reproduce or challenge the result.

### Review Level 4 — System Review

Evaluate subsystem impact on the complete aircraft.

---

## 4. Gate Outcomes

### PASS

The result satisfies the review criteria.

### CONDITIONAL

The result may proceed with explicitly documented limitations or actions.

### FAIL

The result must be corrected before proceeding.

---

## 5. Review Findings

Each finding should include:

* ID,
* severity,
* description,
* evidence,
* affected artifact,
* required action.

---

## 6. Severity

### CRITICAL

Potentially affects safety, flight capability, structural integrity, or fundamental system validity.

### MAJOR

Significant engineering issue requiring correction.

### MINOR

Issue that should be corrected but does not invalidate the primary result.

### INFORMATION

Observation or recommendation.

---

## 7. Independence

The person or agent responsible for producing a critical result should not be the sole verifier of that result.

---

## 8. Review Closure

A review is closed only when:

* findings are resolved or explicitly accepted,
* evidence is documented,
* affected artifacts are updated,
* and the resulting project state is clear.
