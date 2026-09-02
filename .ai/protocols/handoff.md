# ORNITHOPTER Agent Handoff Protocol

## 1. Purpose

This protocol defines how an agent transfers engineering work to another agent.

---

## 2. Handoff Structure

Every significant handoff should contain:

### Task

What was requested?

### Completed Work

What has been done?

### Artifacts

Which files, calculations, simulations, measurements, or decisions were produced?

### Key Results

What are the important results?

### Assumptions

Which assumptions were introduced?

### Uncertainties

What remains uncertain?

### Dependencies

What other work depends on these results?

### Open Questions

What remains unresolved?

### Required Next Action

What should the receiving agent do?

---

## 3. Example

```text
TASK:
Estimate aerodynamic lift at the preliminary cruise condition.

COMPLETED:
Preliminary lift model established.

ARTIFACT:
engineering/aerodynamics/lift-estimate.md

KEY RESULT:
Estimated lift = XXX N.

ASSUMPTIONS:
Steady flow.
Constant air density.
Preliminary wing geometry.

UNCERTAINTIES:
Unsteady flapping effects not included.

DEPENDENCY:
Structures Agent requires estimated peak aerodynamic load.

OPEN QUESTIONS:
Dynamic lift amplification remains unknown.

NEXT ACTION:
Structures Agent should determine preliminary structural load envelope.
```

---

## 4. Handoff Rules

The receiving agent must be able to understand the work without relying on private conversation history.

The sending agent must not omit limitations simply because they complicate the handoff.

---

## 5. Rejection of Handoff

A receiving agent may reject a handoff when:

* essential information is missing,
* assumptions are undocumented,
* units are ambiguous,
* required artifacts are unavailable,
* or the result is insufficiently defined.

The issue must be reported to the System Engineer.

---

## 6. Traceability

Every handoff should identify upstream and downstream artifacts whenever possible.
