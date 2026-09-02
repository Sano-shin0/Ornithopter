# ORNITHOPTER Escalation Protocol

## 1. Purpose

This protocol defines when an engineering issue must be escalated to the System Engineer.

---

## 2. Mandatory Escalation

An agent must escalate when it encounters:

* contradictory requirements,
* missing critical information,
* conflicting specialist results,
* safety-critical uncertainty,
* unexplained physical behavior,
* invalid assumptions,
* impossible performance requirements,
* major interface conflicts,
* significant mass or power budget changes,
* uncertainty that could invalidate the design,
* or a verification failure.

---

## 3. Escalation Format

```text
ESCALATION

Issue:
[description]

Detected by:
[agent]

Affected subsystem:
[subsystem]

Affected artifacts:
[files / IDs]

Severity:
CRITICAL / MAJOR / MINOR

Evidence:
[what demonstrates the issue]

Current assumption:
[if applicable]

Impact:
[engineering consequences]

Recommended action:
[proposed next step]

Decision required:
[what the System Engineer must decide]
```

---

## 4. Safety Escalation

Safety-critical issues must be escalated immediately.

An agent must not continue with a potentially unsafe design merely because the requested task is technically feasible.

---

## 5. Requirement Escalation

If a requirement appears physically impossible or strongly conflicts with another requirement, the agent must not silently relax it.

The conflict must be presented to the System Engineer.

---

## 6. Cross-Disciplinary Escalation

When an issue crosses subsystem boundaries, the System Engineer determines which specialists must participate.

---

## 7. Escalation Does Not Mean Failure

Escalation means that the current agent has identified a decision or uncertainty requiring higher-level coordination.

It is a normal part of engineering development.

---

## 8. Core Principle

> Problems must be escalated while they are still cheap to solve.
