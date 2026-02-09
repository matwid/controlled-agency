# Autonomy Levels v1.0

This document defines a **normative reference model** for agent autonomy.
It is **not** an implementation specification and **not** a maturity model.

The purpose of these levels is to:
- make autonomy **explicit**
- reason about **risk and responsibility**
- prevent accidental escalation of agency

> **Key principle:**  
> Higher autonomy always implies higher risk.  
> There is no “free” autonomy.

---

## Overview

| Level | Name                | Core Characteristic                  |
|------:|---------------------|--------------------------------------|
| L0    | Observer            | No actions, read-only                 |
| L1    | Assistant           | Suggestions, no execution             |
| L2    | Controlled Actor    | Executes within strict boundaries     |
| L3    | Delegated Operator  | Handles tasks with explicit mandate   |
| L4    | Semi-Autonomous     | Operates under continuous constraints |
| L5    | Fully Autonomous    | Explicitly accepted full agency and risk |

---

## L0 — Observer

**Description**  
The agent can observe, analyze, and report.
It has **no ability to act on the environment**.

**Typical capabilities**
- Read data
- Analyze state
- Generate reports
- Highlight anomalies

**Risk profile**
- Minimal
- No side effects possible

**Default recommendation**  
This is the **safest default level** and should be used whenever action is not strictly required.

---

## L1 — Assistant

**Description**  
The agent can generate suggestions and plans,
but **cannot execute actions**.

**Typical capabilities**
- Draft commands or workflows
- Propose decisions
- Simulate outcomes

**Risk profile**
- Low
- Human remains the sole actor

**Key property**
> The agent may influence decisions, but never performs them.

---

## L2 — Controlled Actor

**Description**  
The agent can execute actions,
but **only within narrowly defined technical boundaries**.

**Typical capabilities**
- Perform predefined operations
- Act on whitelisted resources
- Execute reversible actions

**Risk profile**
- Moderate
- Damage is limited by design

**Key requirement**
> All permissions must be technically enforced, not instruction-based.

---

## L3 — Delegated Operator

**Description**  
The agent is entrusted with completing tasks end-to-end
within a clearly scoped mandate.

**Typical capabilities**
- Handle workflows
- Make local decisions
- Recover from expected failures

**Risk profile**
- Elevated
- Requires monitoring and auditability

**Key requirement**
> Mandates must be explicit, time-bound, and revocable.

---

## L4 — Semi-Autonomous Agent

**Description**  
The agent operates continuously within defined constraints
and may initiate actions on its own.

**Typical capabilities**
- Proactive task execution
- Ongoing operation
- Limited self-adjustment within enforced constraints


**Risk profile**
- High
- Failures can cascade if constraints are weak

**Key requirement**
> Continuous enforcement of limits on scope, impact, and cost.

---

## L5 — Fully Autonomous Agent

**Description**  
The agent operates with broad freedom of action
and minimal human oversight.

**Typical capabilities**
- Independent goal pursuit
- Strategy selection
- Action sequencing

**Risk profile**
- Extreme
- Misbehavior has systemic impact

**Position statement**
> L5 is **never a default**.  
> It is an explicit opt-in with consciously accepted risk.

---

## Non-goals of this model

This model does **not**:
- claim that higher levels are better
- imply linear progress or maturity
- prescribe specific implementations

---

## Final note

Autonomy levels exist to support **deliberate choice**.

If you cannot clearly state which level an agent operates at,
the system is already operating outside of defined safety boundaries.