# ORNITHOPTER — Agent Orchestration Protocol

## 1. Purpose

This protocol defines how AI agents collaborate to solve engineering problems within the ORNITHOPTER project.

It defines:

* how tasks enter the AI system;
* how tasks are classified;
* how relevant agents are selected;
* how work is decomposed;
* how agents exchange information;
* how dependencies are managed;
* how independent work is performed;
* how results are integrated;
* how conflicts are resolved;
* how results are verified;
* how failed results trigger feedback loops;
* how changes propagate through the system;
* how tasks are closed.

The purpose of orchestration is not to make every agent participate in every task.

The purpose is to ensure that the **right agents perform the right work in the right order**, while preserving system-level coherence and engineering traceability.

---

# 2. Orchestration Hierarchy

The ORNITHOPTER AI system follows this conceptual hierarchy:

```text
                    PROJECT OWNER
                         │
                         ▼
                       CLAUDE
                         │
                         ▼
                   ORCHESTRATOR
                         │
             ┌───────────┼───────────┐
             │           │           │
             ▼           ▼           ▼
        SPECIALIST   SYSTEM        RESEARCH
          AGENTS     ENGINEER        AGENT
             │           │           │
             └───────────┼───────────┘
                         ▼
                    VERIFICATION
                         │
                         ▼
                  SYSTEM INTEGRATION
                         │
                         ▼
                       RESULT
```

The responsibilities are distinct.

### Claude

Claude is the interface between the project owner and the AI engineering system.

Claude interprets the user's request and operates the orchestration process.

### Orchestrator

The Orchestrator manages workflow execution.

The Orchestrator decides:

* which agents are relevant;
* what order they should work in;
* which tasks can run in parallel;
* when a handoff is required;
* when a result must be verified;
* when a task must loop back;
* when escalation is required;
* when the task can be closed.

The Orchestrator is the **administrator of the agent system**.

### System Engineer

The System Engineer maintains the global engineering view.

The System Engineer is responsible for:

* system-level coherence;
* requirements;
* subsystem interactions;
* engineering trade-offs;
* system constraints;
* interfaces;
* system-level decisions;
* integration.

The System Engineer does not need to personally perform every specialist calculation.

### Specialist Agents

Specialist agents perform domain-specific technical work.

### Verification Agent

The Verification Agent independently challenges important results and evidence.

---

# 3. Fundamental Rule

The Orchestrator coordinates.

The Specialist Agents analyze.

The System Engineer integrates.

The Verification Agent challenges.

Claude communicates the resulting engineering state to the project owner.

No role should silently assume the responsibilities of another role.

---

# 4. Task Intake

Every significant engineering request enters through the Orchestrator.

The Orchestrator first determines:

1. What is being requested?
2. What is the desired output?
3. Is the request technical, organizational, informational, or administrative?
4. Which engineering domains are affected?
5. What existing repository information is relevant?
6. What information is missing?
7. What level of verification is appropriate?

For simple questions, the Orchestrator may resolve the request directly without activating multiple agents.

For significant engineering problems, the full orchestration process should be used.

---

# 5. Task Classification

Before assigning work, classify the task.

Possible categories include:

* Requirement;
* Research;
* Calculation;
* Design;
* Simulation;
* Software;
* Electronics;
* Aerodynamics;
* Structures;
* Mechanisms;
* Propulsion;
* Control;
* Manufacturing;
* Testing;
* Verification;
* System integration;
* Architecture;
* Decision analysis.

A task may belong to multiple categories.

---

# 6. Task Decomposition

Complex tasks must be decomposed into smaller tasks.

Example:

```text
MISSION
  ↓
Determine required flight capability
  ↓
Define aerodynamic requirements
  ↓
Determine wing geometry
  ↓
Estimate lift
  ↓
Determine structural loads
  ↓
Determine actuator requirements
  ↓
Determine power requirement
  ↓
Evaluate control authority
  ↓
Simulate
  ↓
Verify
  ↓
Integrate
```

Each subtask should have:

* objective;
* responsible agent;
* required inputs;
* expected output;
* dependencies;
* verification requirement.

---

# 7. Agent Selection

The Orchestrator selects agents according to the actual technical content.

The Orchestrator must not activate agents merely because they exist.

Examples:

### Aerodynamic Problem

```text
Orchestrator
    ↓
Aerodynamics Agent
    ↓
Simulation Agent
    ↓
Verification Agent
```

### Structural Problem

```text
Orchestrator
    ↓
Structures Agent
    ↓
Manufacturing Agent
    ↓
Verification Agent
```

### Flapping Mechanism

```text
Orchestrator
    ↓
Mechanisms Agent
    ↓
Structures Agent
    ↓
Propulsion Agent
    ↓
Control Agent
    ↓
Verification Agent
```

### Software Problem

```text
Orchestrator
    ↓
Software Agent
    ↓
Verification Agent
```

The exact chain depends on the problem.

---

# 8. Specialist Independence

Specialist agents should perform their analysis independently when possible.

For example:

```text
                 ┌── Aerodynamics
                 │
Problem ─────────┼── Structures
                 │
                 ├── Propulsion
                 │
                 └── Control
```

The purpose of parallel analysis is to reduce unnecessary dependency and allow independent technical perspectives.

The Orchestrator later integrates the outputs.

---

# 9. Parallel vs Sequential Work

Tasks may be executed in parallel when they do not depend on one another.

Example:

```text
System Requirements
        │
        ├── Aerodynamic Study
        ├── Structural Study
        ├── Mechanism Study
        └── Electronics Study
```

However, if:

```text
A → B
```

then B must not be treated as final until A has produced sufficiently reliable information.

Example:

```text
Wing Geometry
      ↓
Aerodynamic Analysis
      ↓
Aerodynamic Loads
      ↓
Structural Analysis
      ↓
Structural Design
```

---

# 10. Dependency Graph

The Orchestrator should maintain awareness of dependencies between tasks.

Dependencies may be:

* technical;
* numerical;
* informational;
* physical;
* architectural;
* verification-related.

A task may be marked:

* `BLOCKED`;
* `READY`;
* `IN_PROGRESS`;
* `WAITING`;
* `REVIEW`;
* `VERIFIED`;
* `FAILED`;
* `COMPLETE`.

The status must reflect the actual state of the work.

---

# 11. Standard Task Lifecycle

A significant engineering task generally follows:

```text
MISSION
   ↓
UNDERSTAND
   ↓
SPECIFY
   ↓
DECOMPOSE
   ↓
ASSIGN
   ↓
RESEARCH
   ↓
CALCULATE / DESIGN
   ↓
SIMULATE
   ↓
INTEGRATE
   ↓
VERIFY
   ↓
TEST
   ↓
VALIDATE
   ↓
UPDATE SYSTEM STATE
   ↓
CLOSE
```

Not every task requires every stage.

The Orchestrator determines the appropriate path.

---

# 12. Understanding Stage

Before technical work begins, the Orchestrator must establish:

* the objective;
* the desired output;
* relevant constraints;
* known information;
* missing information;
* affected subsystems;
* expected evidence level.

If the request is ambiguous in a way that materially affects the result, clarification should be requested.

---

# 13. Specification Stage

Where appropriate, convert the objective into explicit requirements.

Requirements should be:

* understandable;
* measurable where possible;
* testable;
* traceable.

Example:

```text
Objective:
The aircraft must remain airborne.

Engineering requirement:
The system shall generate sufficient average lift to support its operating mass under the defined flight condition.
```

The requirement should not unnecessarily prescribe the implementation.

---

# 14. Research Stage

Research is performed when existing knowledge is insufficient.

The Research Agent may provide:

* scientific literature;
* engineering references;
* biological references;
* material properties;
* known technologies;
* existing designs;
* relevant experimental data;
* equations;
* design precedents.

Research outputs must distinguish:

* source-backed facts;
* interpretations;
* assumptions;
* hypotheses.

---

# 15. Calculation Stage

Calculations must identify:

* inputs;
* assumptions;
* equations;
* units;
* results;
* limitations.

Important calculations should be independently checked when appropriate.

The Orchestrator should request verification when:

* the result is critical;
* the result drives a major design decision;
* the result is safety-relevant;
* the result appears unusual;
* the result has significant uncertainty.

---

# 16. Design Stage

Design work should consider:

* requirements;
* physical constraints;
* mass;
* power;
* energy;
* manufacturability;
* interfaces;
* control;
* safety;
* reliability;
* performance.

A design proposal is not automatically an approved project decision.

---

# 17. Simulation Stage

When simulation is appropriate:

```text
Model Definition
      ↓
Assumptions
      ↓
Parameters
      ↓
Numerical Implementation
      ↓
Execution
      ↓
Results
      ↓
Physical Plausibility
      ↓
Verification
```

A simulation must identify its assumptions and limitations.

A simulation result must never be presented as experimental validation.

---

# 18. Agent Result Format

A significant agent result should contain, when applicable:

```text
TASK
OBJECTIVE
INPUTS
ASSUMPTIONS
METHOD
RESULTS
LIMITATIONS
OPEN QUESTIONS
RECOMMENDATION
DEPENDENCIES
VERIFICATION STATUS
```

This allows another agent to understand and reuse the result.

---

# 19. Handoff

When work passes from one agent to another, the relevant information must be transferred explicitly.

A handoff should contain:

* source agent;
* receiving agent;
* objective;
* relevant inputs;
* assumptions;
* results;
* uncertainties;
* required next action;
* dependencies.

The detailed handoff rules are defined in:

`.ai/protocols/handoff.md`

---

# 20. Agent Communication

Agents should communicate only information relevant to the engineering task.

Communication should be:

* explicit;
* concise;
* technically precise;
* traceable;
* free of unsupported claims.

An agent must not assume another agent has access to information that was not provided or stored.

---

# 21. Intermediate Results

Intermediate results may be used before final verification when necessary.

However, they must be clearly marked as:

* preliminary;
* provisional;
* unverified;
* estimated.

Preliminary information must not silently become validated project knowledge.

---

# 22. Integration

After specialist work, the Orchestrator coordinates integration.

The System Engineer evaluates whether the results are compatible.

Integration should consider:

* geometry;
* mass;
* center of gravity;
* inertia;
* power;
* energy;
* loads;
* control;
* timing;
* interfaces;
* manufacturing;
* safety.

A set of individually correct subsystem results does not automatically constitute a correct aircraft.

---

# 23. System Engineer Integration Gate

The System Engineer should review important integrated results before they become part of the system baseline.

The System Engineer asks:

* Are the subsystem assumptions compatible?
* Are the interfaces compatible?
* Are the requirements satisfied?
* Are the budgets consistent?
* Are there contradictions?
* Are important uncertainties understood?
* Does the design remain physically plausible?

If not, the Orchestrator must reopen the relevant work.

---

# 24. Verification Gate

Important results must pass through the Verification Agent when appropriate.

```text
Engineering Result
       ↓
Verification
       ↓
 ┌─────┼──────────┐
 ↓     ↓          ↓
PASS  CONDITIONAL FAIL
```

### PASS

The result may proceed.

### CONDITIONAL

The result may proceed with explicitly documented limitations or required actions.

### FAIL

The result cannot be accepted as currently established.

---

# 25. Verification Independence

The Verification Agent must not simply repeat the same reasoning as the original agent.

Verification should challenge:

* assumptions;
* calculations;
* implementation;
* evidence;
* units;
* boundary conditions;
* physical plausibility;
* requirements;
* interfaces;
* test quality.

The purpose is to detect errors, not merely confirm them.

---

# 26. Verification Failure Loop

A failed verification must trigger a controlled feedback loop.

```text
Verification FAIL
       ↓
Identify cause
       ↓
Identify earliest affected stage
       ↓
Reopen affected work
       ↓
Correct / Research / Recalculate / Redesign
       ↓
Re-integrate
       ↓
Verify again
```

The entire project must not automatically restart.

The Orchestrator determines the earliest stage that must be reopened.

---

# 27. Example Feedback Loop

Suppose a simulation produces an impossible result.

```text
Simulation
    ↓
Verification
    ↓
FAIL
    ↓
Check implementation
    ↓
Implementation correct
    ↓
Check assumptions
    ↓
Assumption invalid
    ↓
Research
    ↓
Updated model
    ↓
Simulation
    ↓
Verification
```

The loop stops when the result satisfies the appropriate acceptance criteria.

---

# 28. Conflict Resolution

Agents may produce contradictory conclusions.

When this occurs:

```text
Agent A ─────┐
             │
             ▼
          CONFLICT
             ▲
             │
Agent B ─────┘
             ↓
       Compare assumptions
             ↓
       Compare methods
             ↓
       Compare evidence
             ↓
       Assess system impact
             ↓
      System Engineer review
             ↓
       Resolve / Investigate
```

The Orchestrator coordinates the process.

The System Engineer makes the system-level engineering judgment.

The final reasoning should be documented when significant.

---

# 29. No Majority Voting

Engineering conflicts must not be resolved by counting agents.

For example:

```text
3 agents say A
1 agent says B
```

does not mean A is automatically correct.

The decision must be based on:

* evidence;
* assumptions;
* physical reasoning;
* model validity;
* experimental data;
* requirements;
* uncertainty.

---

# 30. Escalation

The Orchestrator should escalate when:

* information is missing;
* agents disagree materially;
* requirements conflict;
* evidence is insufficient;
* a safety concern appears;
* a system-level decision is required;
* an external human decision is required.

Detailed escalation rules are defined in:

`.ai/protocols/escalation.md`

---

# 31. Human Decision Gate

Some decisions require explicit project-owner approval.

Examples may include:

* major architecture changes;
* significant budget changes;
* irreversible manufacturing decisions;
* major safety decisions;
* project priorities;
* major performance trade-offs;
* final design selection.

The AI system may recommend a decision but must not falsely represent it as approved.

---

# 32. Change Propagation

A significant engineering change must trigger an impact analysis.

```text
CHANGE
  ↓
Identify affected elements
  ↓
Identify dependent calculations
  ↓
Identify affected simulations
  ↓
Identify affected interfaces
  ↓
Identify affected tests
  ↓
Recalculate / Redesign
  ↓
Re-simulate if required
  ↓
Re-verify
  ↓
Update System State
```

Example:

```text
Wing Geometry Changed
        ↓
Aerodynamics
        ↓
Loads
        ↓
Structures
        ↓
Mechanism
        ↓
Control
        ↓
Power
        ↓
Simulation
        ↓
Verification
```

The Orchestrator determines which branches are actually affected.

---

# 33. Change Impact Levels

Changes may be classified approximately as:

### Level 0 — Informational

No engineering consequence.

### Level 1 — Local

Affects only one limited analysis or document.

### Level 2 — Subsystem

Affects a subsystem and potentially its interfaces.

### Level 3 — Cross-System

Affects several subsystems.

### Level 4 — System Baseline

Affects fundamental requirements, architecture, or validated system behavior.

Higher-impact changes require more extensive review.

---

# 34. Reuse of Previous Results

Previously established results may be reused when:

* their assumptions remain valid;
* their inputs remain valid;
* their configuration is compatible;
* their verification status is known.

If a change invalidates those conditions, the result must be reconsidered.

A result must never be reused blindly merely because it exists in the repository.

---

# 35. System State

The Orchestrator and System Engineer must maintain awareness of:

* current requirements;
* current design baseline;
* validated results;
* assumptions;
* open questions;
* unresolved risks;
* failed analyses;
* verification status;
* subsystem maturity;
* pending changes.

The system state should represent what is actually known.

---

# 36. Knowledge States

Engineering knowledge should be treated as having different states.

Possible states include:

```text
UNKNOWN
   ↓
ASSUMED
   ↓
PROPOSED
   ↓
ANALYZED
   ↓
SIMULATED
   ↓
TESTED
   ↓
VERIFIED
   ↓
VALIDATED
```

These states must not be confused.

For example:

```text
ASSUMED ≠ VERIFIED
SIMULATED ≠ TESTED
TESTED ≠ VALIDATED
```

---

# 37. Task Iteration

Engineering tasks may require multiple iterations.

A normal loop may be:

```text
Design
  ↓
Calculate
  ↓
Simulate
  ↓
Verify
  ↓
Design Revision
  ↓
Calculate
  ↓
Simulate
  ↓
Verify
```

Iteration is expected.

The Orchestrator should stop unnecessary iterations when additional work no longer provides meaningful improvement.

---

# 38. Stop Conditions

The Orchestrator may close a task when:

* the objective has been satisfied;
* required artifacts exist;
* necessary calculations are complete;
* relevant verification is complete;
* assumptions are documented;
* remaining uncertainty is understood;
* downstream dependencies are identified;
* no unresolved critical conflict remains.

A task should remain open if a critical dependency is unresolved.

---

# 39. Blocked Tasks

A task is `BLOCKED` when progress cannot reasonably continue because required information or work is missing.

Example:

```text
Actuator sizing
      ↓
Requires motor torque
      ↓
Motor torque unknown
      ↓
BLOCKED
```

The Orchestrator should identify what is blocking the task and determine which agent or human can resolve it.

---

# 40. Deadlock Prevention

If agents repeatedly depend on one another:

```text
Agent A → Agent B
Agent B → Agent A
```

the Orchestrator must identify the circular dependency.

It should then:

1. identify the minimum information required;
2. establish a temporary assumption if appropriate;
3. request a human decision if necessary;
4. break the dependency logically;
5. document the assumption.

The system must not remain indefinitely in an unresolved loop.

---

# 41. Resource Management

The Orchestrator should avoid unnecessary agent activation.

Do not activate:

* all agents;
* all workflows;
* all protocols

for every question.

Use the minimum set of agents necessary to produce a reliable result.

However, insufficient agent involvement must not be used as a reason to skip necessary verification.

---

# 42. Parallelization Rule

Parallel work is preferred when:

* tasks are independent;
* inputs are already available;
* outputs can later be integrated.

Sequential work is preferred when:

* one task depends directly on another;
* a previous result defines the next input;
* consistency requires a common baseline.

---

# 43. Agent Failure

If an agent cannot complete its assigned task, it must report:

* what it attempted;
* what prevented completion;
* what information is missing;
* what partial result exists;
* what should happen next.

The Orchestrator then decides whether to:

* retry;
* reassign;
* provide additional information;
* change the method;
* escalate.

Failure must not be hidden.

---

# 44. Tool Failure

If a tool, simulation, software package, or external resource fails:

```text
Tool Failure
    ↓
Identify failure
    ↓
Determine whether result is affected
    ↓
Retry / replace / investigate
    ↓
Document limitation
```

A failed tool execution must never be represented as a successful result.

---

# 45. External Information

When external information is used, the Research Agent or relevant specialist should identify:

* source;
* relevance;
* date when important;
* reliability;
* limitations.

External information must not automatically become a project requirement.

It must be interpreted in the context of ORNITHOPTER.

---

# 46. Evidence Hierarchy

When resolving technical disagreement, evidence should generally be considered in this order:

1. validated experimental evidence;
2. independently verified experimental data;
3. verified analytical calculations;
4. validated numerical models;
5. unverified simulations;
6. theoretical reasoning;
7. engineering estimates;
8. assumptions;
9. speculation.

This hierarchy is contextual and does not mean experimental data is automatically correct.

Data quality must still be evaluated.

---

# 47. Biological Inspiration

ORNITHOPTER is a bio-inspired flapping-wing aircraft.

Biological observations may inform:

* wing morphology;
* wing flexibility;
* flapping kinematics;
* control strategies;
* tail behavior;
* stability;
* energy management;
* takeoff;
* landing;
* gliding.

However, biological similarity does not automatically prove engineering suitability.

Biological observations must be translated into measurable engineering parameters.

---

# 48. Prototype-Oriented Iteration

The orchestration system must support progression from theory to physical prototypes.

```text
Research
  ↓
Concept
  ↓
Analysis
  ↓
Simulation
  ↓
Prototype
  ↓
Component Test
  ↓
Subsystem Test
  ↓
System Test
  ↓
Flight Test
  ↓
Validation
```

Results from physical testing must feed back into the models.

---

# 49. Experimental Feedback Loop

Experimental evidence should update the engineering system.

```text
Prototype
   ↓
Test
   ↓
Measurement
   ↓
Analysis
   ↓
Compare with Model
   ↓
Difference
   ↓
Investigate
   ↓
Update Model / Design
   ↓
Retest
```

The objective is continuous convergence between:

* model;
* simulation;
* prototype;
* physical reality.

---

# 50. Verification and Validation Loop

The overall engineering loop is:

```text
Requirement
    ↓
Design
    ↓
Analysis
    ↓
Simulation
    ↓
Verification
    ↓
Prototype
    ↓
Testing
    ↓
Validation
    ↓
System Update
    ↓
New Requirement / Improvement
```

The project is iterative rather than strictly linear.

---

# 51. Orchestrator Decision Logic

For every significant task, the Orchestrator should conceptually evaluate:

```text
1. What is the task?
2. What does the repository already know?
3. What information is missing?
4. Which agents are relevant?
5. Which tasks depend on one another?
6. Which tasks can run in parallel?
7. What evidence is required?
8. What must be verified?
9. What happens if verification fails?
10. What other subsystems could be affected?
11. Is human approval required?
12. When can the task be closed?
```

---

# 52. Minimal Orchestration

Not every request needs a large workflow.

Example:

> "What does Reynolds number mean?"

Possible process:

```text
Claude
  ↓
Direct explanation
```

No multi-agent orchestration is required.

---

# 53. Moderate Orchestration

Example:

> "What material should we consider for the wing spar?"

Possible process:

```text
Orchestrator
   ↓
Research Agent
   ↓
Structures Agent
   ↓
Manufacturing Agent
   ↓
System Engineer
   ↓
Verification
```

---

# 54. Full Orchestration

Example:

> "Design a flapping wing capable of supporting the aircraft for flight."

Possible process:

```text
                         Orchestrator
                              │
                              ▼
                       System Engineer
                              │
            ┌─────────────────┼─────────────────┐
            ▼                 ▼                 ▼
        Research        Aerodynamics        Structures
            │                 │                 │
            └─────────────────┼─────────────────┘
                              ▼
                         Mechanisms
                              │
                              ▼
                          Propulsion
                              │
                              ▼
                           Control
                              │
                              ▼
                         Simulation
                              │
                              ▼
                        Integration
                              │
                              ▼
                        Verification
                              │
                         ┌────┴────┐
                         │         │
                       PASS       FAIL
                         │         │
                         │         ▼
                         │      Reopen
                         │      affected
                         │       stage
                         │         │
                         │         └──────→ Loop
                         ▼
                   System Baseline
```

---

# 55. No Automatic Approval

Completion of an agent task does not automatically approve its result.

For example:

```text
Aerodynamics Agent: COMPLETE
```

does not mean:

```text
Aerodynamic result: VERIFIED
```

Likewise:

```text
Simulation Agent: COMPLETE
```

does not mean:

```text
Simulation: VALIDATED
```

The appropriate verification state must be explicitly established.

---

# 56. Final Integration Gate

Before an important result becomes part of the system baseline:

```text
Specialist Results
       ↓
Consistency Check
       ↓
System Engineer
       ↓
Verification
       ↓
Acceptance
       ↓
System State Update
```

If the result fails integration, the relevant work must be reopened.

---

# 57. System Baseline

The system baseline represents the currently accepted engineering configuration.

It may include:

* requirements;
* geometry;
* mass;
* components;
* interfaces;
* software versions;
* parameters;
* validated models;
* verified calculations;
* test results.

Changes to the baseline must be traceable.

---

# 58. Traceability

Important information should be traceable through:

```text
Requirement
    ↓
Decision
    ↓
Analysis
    ↓
Design
    ↓
Implementation
    ↓
Test
    ↓
Verification
    ↓
Validation
```

The goal is to make important engineering decisions reconstructable.

---

# 59. No Fabricated State

The Orchestrator must never claim that:

* an agent performed work when it did not;
* a file was inspected when it was not;
* a calculation was executed when it was not;
* a simulation was run when it was not;
* a test passed when it did not;
* a result was verified when it was not;
* a requirement was approved when it was not.

Unknown information must remain unknown.

---

# 60. Orchestration Log

For important multi-agent tasks, the system should maintain enough information to reconstruct:

* task;
* agents involved;
* decisions;
* important handoffs;
* important assumptions;
* verification status;
* unresolved issues;
* final outcome.

The exact storage mechanism may evolve with the project.

---

# 61. Review Protocol

Important integrated results should use:

`.ai/protocols/review-protocol.md`

The review should consider:

* correctness;
* completeness;
* consistency;
* evidence;
* assumptions;
* interfaces;
* risks;
* verification status.

---

# 62. Agent Protocol

Individual agent behavior is governed by:

`.ai/protocols/agent-protocol.md`

The orchestration protocol defines **how agents collaborate**.

The agent protocol defines **how an individual agent behaves**.

These protocols must remain complementary.

---

# 63. Handoff Protocol

Agent-to-agent transfers are governed by:

`.ai/protocols/handoff.md`

The Orchestrator must use the handoff protocol for significant transfers of responsibility.

---

# 64. Escalation Protocol

Escalation is governed by:

`.ai/protocols/escalation.md`

The Orchestrator must use escalation when normal agent collaboration cannot resolve an issue.

---

# 65. Workflow Integration

When an existing workflow applies, the Orchestrator should use the appropriate workflow from:

`.ai/workflows/`

Examples include:

* research;
* specify;
* calculate;
* design;
* simulate;
* verify.

Workflows define repeatable task processes.

Agents provide domain expertise.

Protocols define interaction.

The Constitution defines fundamental project rules.

---

# 66. Priority of Rules

The effective hierarchy is:

```text
Project Owner
      ↓
Constitution
      ↓
CLAUDE.md
      ↓
Protocols
      ↓
Rules
      ↓
Workflows
      ↓
Agent Instructions
      ↓
Task-Specific Instructions
```

Lower-level instructions must not contradict higher-level project rules.

When a conflict exists, the conflict must be identified and resolved rather than silently ignored.

---

# 67. Orchestration Loop — Master Algorithm

The complete orchestration loop is:

```text
┌─────────────────────────────┐
│        RECEIVE TASK         │
└──────────────┬──────────────┘
               ↓
┌─────────────────────────────┐
│        UNDERSTAND           │
└──────────────┬──────────────┘
               ↓
┌─────────────────────────────┐
│        CHECK REPOSITORY      │
└──────────────┬──────────────┘
               ↓
┌─────────────────────────────┐
│       IDENTIFY MISSING       │
│          INFORMATION         │
└──────────────┬──────────────┘
               ↓
┌─────────────────────────────┐
│        CLASSIFY TASK         │
└──────────────┬──────────────┘
               ↓
┌─────────────────────────────┐
│       DECOMPOSE TASK         │
└──────────────┬──────────────┘
               ↓
┌─────────────────────────────┐
│        SELECT AGENTS         │
└──────────────┬──────────────┘
               ↓
┌─────────────────────────────┐
│       EXECUTE WORK           │
│   parallel / sequential      │
└──────────────┬──────────────┘
               ↓
┌─────────────────────────────┐
│        HANDOFF RESULTS       │
└──────────────┬──────────────┘
               ↓
┌─────────────────────────────┐
│         INTEGRATE            │
└──────────────┬──────────────┘
               ↓
┌─────────────────────────────┐
│         VERIFY               │
└──────────────┬──────────────┘
               ↓
        ┌──────┴──────┐
        │             │
      PASS        CONDITIONAL
        │             │
        │             ▼
        │      Document limits
        │      + required actions
        │             │
        │             ▼
        │          Continue
        │
        ▼
      ACCEPT
        │
        │
        └──────────────────┐
                           │
                           ▼
                         FAIL
                           │
                           ▼
                  IDENTIFY EARLIEST
                    AFFECTED STAGE
                           │
                           ▼
                     REOPEN WORK
                           │
                           ▼
                       ITERATE
                           │
                           └──────────→ EXECUTE WORK


After acceptance:

ACCEPT
  ↓
UPDATE SYSTEM STATE
  ↓
CHECK DOWNSTREAM DEPENDENCIES
  ↓
CHECK HUMAN APPROVAL
  ↓
CLOSE TASK
```

---

# 68. Core Orchestration Principles

The ORNITHOPTER orchestration system follows these principles:

1. **Use the minimum necessary agents.**
2. **Never skip required verification.**
3. **Never treat assumptions as facts.**
4. **Never treat simulations as experimental validation.**
5. **Never resolve technical disagreement by majority vote.**
6. **Never fabricate work or results.**
7. **Never silently change system-level decisions.**
8. **Always consider cross-domain effects.**
9. **Always preserve traceability for important decisions.**
10. **Reopen only the affected part of the workflow when possible.**
11. **Use parallel work when dependencies permit it.**
12. **Use sequential work when dependencies require it.**
13. **Escalate when the AI system cannot safely resolve an issue.**
14. **Maintain the distinction between coordination and engineering authority.**
15. **Treat the physical aircraft as the final reality against which models must ultimately be validated.**

---

# 69. Final Principle

The purpose of orchestration is not to make the AI system appear complex.

The purpose is to make the engineering process reliable.

The fundamental loop is:

```text
UNDERSTAND
    ↓
PLAN
    ↓
ASSIGN
    ↓
ANALYZE
    ↓
INTEGRATE
    ↓
VERIFY
    ↓
ITERATE IF NECESSARY
    ↓
VALIDATE
    ↓
UPDATE
```

The Orchestrator coordinates the process.

The specialists provide technical expertise.

The System Engineer maintains system coherence.

The Verification Agent challenges the evidence.

Claude communicates the resulting engineering state.

The project owner retains final authority over project decisions.

> **The goal of orchestration is not to produce more AI activity. It is to produce better engineering decisions with traceable evidence.**
