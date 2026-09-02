# ORNITHOPTER Preliminary Power Budget

**Status:** DRAFT
**Revision:** 0.1

---

# 1. Objective

Determine the approximate mechanical and electrical power required for flapping-wing flight.

---

# 2. Power Chain

The system shall be modeled as:

```text
Battery
   ↓
Electrical Power
   ↓
Actuator
   ↓
Mechanical Power
   ↓
Flapping Mechanism
   ↓
Wing Motion
   ↓
Aerodynamic Power
   ↓
Flight
```

Each stage has associated losses.

---

# 3. Electrical Power

The electrical power consumed by the actuator is:

$$
P_{elec}=VI
$$

where:

* \(V\) = electrical voltage,
* \(I\) = electrical current.

---

# 4. Actuator Efficiency

If actuator efficiency is:

$$
\eta_{act}
$$

then:

$$
P_{mech}
=
\eta_{act}P_{elec}
$$

---

# 5. Mechanism Efficiency

If mechanism efficiency is:

$$
\eta_{mech}
$$

then:

$$
P_{wing}
=
\eta_{mech}P_{mech}
$$

Therefore:

$$
P_{wing}
=
\eta_{act}\eta_{mech}P_{elec}
$$

---

# 6. Aerodynamic Power

The aerodynamic power requirement shall eventually be estimated from the flapping-wing aerodynamic model.

A simplified propulsive relationship may initially be investigated:

$$
P_{aero}=TV
$$

where:

* \(T\) = mean propulsive force,
* \(V\) = forward velocity.

This relationship alone is insufficient for the final flapping-wing model because aerodynamic power is also associated with unsteady wing motion.

---

# 7. Total System Power

The total electrical power shall include:

$$
P_{total}
=
P_{actuation}
+
P_{electronics}
+
P_{sensors}
+
P_{communication}
+
P_{other}
$$

---

# 8. Energy Requirement

For flight duration \(t\):

$$
E=P_{total}t
$$

Battery capacity shall be determined from the required usable energy.

---

# 9. Endurance

A preliminary endurance estimate is:

$$
t
=
\frac{E_{usable}}{P_{total}}
$$

The usable battery energy shall account for:

* conversion losses,
* battery discharge limits,
* temperature,
* safety margins,
* and degradation.

---

# 10. Gliding

Gliding shall be considered as a separate power state.

During idealized gliding:

$$
P_{actuation}\rightarrow 0
$$

or is significantly reduced.

This may allow substantial energy savings depending on the aerodynamic efficiency of the configuration.

---

# 11. Power Sensitivity

The following parameters shall be investigated:

* total mass,
* wing area,
* flapping frequency,
* stroke amplitude,
* airspeed,
* actuator efficiency,
* mechanism efficiency,
* wing flexibility,
* battery mass.

---

# 12. Battery-Mass Feedback

Battery mass shall not be treated as independent of endurance.

Increasing battery capacity increases:

$$
m_{battery}
$$

which increases:

$$
W=mg
$$

which increases the aerodynamic requirement and potentially increases power consumption.

Therefore battery sizing shall be solved iteratively.

---

# 13. Current Status

No actuator or battery has been selected.

Power requirements shall be derived after the first aerodynamic and mass estimates are available.
