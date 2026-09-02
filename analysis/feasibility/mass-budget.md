# ORNITHOPTER Preliminary Mass Budget

**Status:** DRAFT
**Revision:** 0.1

---

# 1. Purpose

This document defines the preliminary mass budget for ORNITHOPTER.

The objective is to estimate the total mass of the system and determine how mass influences the aerodynamic and energetic requirements.

---

# 2. Mass Model

The total mass shall be modeled as:

$$
m_{total} =
m_{body}
+m_{wings}
+m_{mechanism}
+m_{actuator}
+m_{battery}
+m_{electronics}
+m_{sensors}
+m_{wiring}
+m_{structure}
+m_{other}
$$

The corresponding weight is:

$$
W=m_{total}g
$$

where:

$$
g=9.81\;m/s^2
$$

---

# 3. Preliminary Mass Table

| Subsystem          |    Mass | Status      | Confidence |
| ------------------ | ------: | ----------- | ---------- |
| Body               |     TBD | Estimated   | Low        |
| Left wing          |     TBD | Estimated   | Low        |
| Right wing         |     TBD | Estimated   | Low        |
| Flapping mechanism |     TBD | Unknown     | Low        |
| Actuator           |     TBD | Unknown     | Low        |
| Battery            |     TBD | Unknown     | Low        |
| Electronics        |     TBD | Estimated   | Low        |
| Sensors            |     TBD | Estimated   | Low        |
| Wiring             |     TBD | Estimated   | Low        |
| Structure          |     TBD | Estimated   | Low        |
| Other              |     TBD | Estimated   | Low        |
| **Total**          | **TBD** | **Derived** | **Low**    |

---

# 4. Mass Distribution

The project shall track not only total mass but also its distribution.

Important quantities include:

* center of gravity,
* wing mass,
* body mass,
* actuator mass,
* battery position,
* and inertial properties.

Mass distribution shall be considered in the flight-dynamics analysis.

---

# 5. Mass Sensitivity

The effect of total mass on required aerodynamic force shall be evaluated.

For a system in steady vertical force equilibrium:

$$
L \approx mg
$$

Therefore:

$$
\frac{\Delta L}{L}
\approx
\frac{\Delta m}{m}
$$

This means that increasing mass directly increases the required aerodynamic force.

---

# 6. Iterative Mass Budget

The mass budget shall be updated as subsystem designs become available.

The following feedback loop shall be maintained:

```text
Initial Mass Estimate
        ↓
Aerodynamic Requirements
        ↓
Actuator Requirements
        ↓
Battery Requirements
        ↓
Updated Mass
        ↓
Updated Aerodynamic Requirements
        ↓
Iteration
```

---

# 7. Current Status

No final mass target has been established.

The project intentionally avoids imposing an arbitrary maximum mass before aerodynamic feasibility is understood.
