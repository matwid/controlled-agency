# Why not just an LLM + scripts?

This is a reasonable question — and often the right starting point.

For many tasks, a language model (such as ChatGPT or similar tools),
combined with scripts, cron jobs, or glue code,
can be sufficient **when used in an ad-hoc or experimental context**.

This includes early prototypes and early-stage agent runtimes.

However, once systems move from **experimentation** to **operation**,
several structural limitations emerge.

---

## 1. Scripts assume determinism — agents do not

Scripts execute predefined logic.
Agentic systems make decisions under uncertainty.

Once decision-making is introduced, scripts alone no longer provide:
- clear responsibility
- predictable behavior
- bounded failure modes

---

## 2. Prompts are not boundaries

In ad-hoc setups, safety relies on:
- prompt wording
- conventions
- “the model usually does the right thing”

These are expectations, not controls.

When something goes wrong, there is no technical mechanism
that prevents the agent from exceeding its intended scope.

---

## 3. Autonomy escalates silently

In script-based setups, autonomy often increases unintentionally:
- one more permission
- one more retry
- one more integration

Without an explicit autonomy model,
systems drift into higher-risk behavior without notice.

---

## 4. There is no explicit blast radius

Ad-hoc automation rarely defines:
- maximum impact
- worst-case damage
- acceptable loss

Failures are discovered **after** they occur.

---

## 5. Cost is treated as an afterthought

Retry loops, model escalation, and uncontrolled execution
can silently turn into operational incidents.

Without enforced limits, cost becomes another failure mode.

---

## When LLMs + scripts are enough

- One-off tasks
- Experiments
- Personal tooling
- Situations with minimal downstream impact

---

## When they are not

- Continuous operation
- Shared environments
- Production systems
- Regulated or accountable contexts

---

## The difference is not intelligence — it is governance

The question is not whether a system can perform a task.

The question is whether its behavior is:
- bounded
- observable
- auditable
- defensible

Controlled agency addresses this gap.

### A note on agent runtimes

This document does not argue against agent runtimes or orchestration frameworks.

Projects like OpenClaw provide powerful foundations for agentic systems.
The question addressed here is not capability,
but how such systems are **operated, constrained, and governed**
once they are deployed in real, accountable environments.
