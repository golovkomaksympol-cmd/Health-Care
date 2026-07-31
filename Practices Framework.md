# Practices Framework

The meta-framework used to design, score, and triage every practice in a patient's stack. Built around **Theory of Constraints**: bandwidth is the real bottleneck, not knowledge or money.

## The bottleneck

For most patients in this repo, the binding constraints are:

- **Time** — minutes available for health-related activity.
- **Cognitive load (attention)** — how much can be planned, decided, and tracked.
- **Social capital** — patience and support of partners/family for protocol-driven life.

What's typically **not** the constraint: money, information access, current health level. So the framework optimizes the time/attention/social budget, not the information budget.

## The three operational vectors

### Vector 1: Impact (System gain)

Each practice is rated on three dimensions of how much it actually moves the system.

**Leverage** — magnitude of physiological shift at perfect execution:

- **(3) Foundational** — changes base architecture (muscles, vessels, metabolism, hormones).
- **(2) Routing** — improves absorption / signaling / direction of resources.
- **(1) Micro-patch** — benefit is within 1-3% statistical noise.

**Compounding** — ability to generate "compound interest":

- **(3) Exponential** — improves the function of *other* systems. Sleep is the canonical example: better sleep → better decisions → better food → better sleep.
- **(2) Cumulative** — improves only its own metric, but builds with time.
- **(1) Transactional** — one-shot effect, resets the next day.

**Latency** — how fast the system gives feedback:

- **Real-time** — hours/days. Visible result gives quick dopamine, easy to sustain motivation.
- **Delayed** — weeks/months. Requires discipline; result only visible on labs.

### Vector 2: Friction (System cost)

How much bandwidth the practice consumes.

**Direct cost** (time / attention / social):

- **(3) High** — >40 min, requires isolation from family, hard willpower.
- **(2) Medium** — 15-30 min, requires light planning.
- **(1) Low** — <5 min, embeds into routine, near-zero social friction.

**Minimum Effective Dose (MED)** — the line beyond which additional minutes stop paying off. The goal is to find the point where 20% of effort generates 80% of the adaptation (e.g., one Norwegian-4×4 session per week instead of three, to maintain VO2 max).

**Decay Rate** — how unforgiving the practice is to missed days:

- **(3) High tolerance** — gains stick for weeks even if fully skipped.
- **(2) Medium** — degradation begins after a few days.
- **(1) Low / fragile** — one missed day undoes the result.

### Vector 3: Operational States (the Defcon ladder)

Protocol for gracefully shutting down modules as the bandwidth bottleneck tightens. Transitions to lower levels are **legitimate, conscious, and guilt-free** — that's the point of having them.

- **Level 0 (Safe Mode / Survival)** — hard crisis, illness, jetlag, work emergency. Goal: don't cascade. Only sleep (as much as possible) and protection from toxic inputs (no alcohol, no sugar, no junk food). Everything else paused.
- **Level 1 (Low Power / Resource deficit)** — hard week, family overload. All plugins and complex calculations off. Keep: baseline sleep, protein in every meal, any background movement (walking, stairs).
- **Level 2 (Normal Operation / Baseline)** — ordinary routine. Full stack: planned training (Zone 2 + intervals), curated nutrition, baseline supplements, wearable metrics collected.
- **Level 3 (Architect Mode / Resource surplus)** — weekend, vacation, light days. Capital-improvement time: lab work, literature reading, deep meditation sessions, stack revision, protocol testing.

On Level 1, complex practices don't disappear — they collapse to their **Minimum Effective Dose**. E.g., McGill Big 3 collapses to one set of plank; strength session collapses to a single compound lift.

## The scoring rubric in use

When designing or pruning a stack:

- Rate each candidate practice on (Leverage, Compounding, Latency, Direct Cost, Decay Rate).
- Anything with **Leverage = 1** is a candidate to cut unless cost is also 1.
- Anything with **Compounding = 3** earns extra weight even if Latency is slow.
- Anything with **Decay Rate = 1** (fragile) is risky as a baseline — promote to plugin-only.

## Where the per-patient dashboard lives

Each patient's actual scored stack belongs in their `Medical Profile.md` (in a "Current Stack Dashboard" section) — not here. This file defines the scoring system; the patient file applies it to their specific practices.
