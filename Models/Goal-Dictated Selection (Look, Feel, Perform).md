# Goal-Dictated Selection — Look / Feel / Perform (Andy Galpin)

A **dosing decision-rule**: what you're training *for* fixes the effort-proximity and frequency you must use, and those two cannot be maximised together. Entry point for `plan-workout` — no session is designed before the driver is named.

Not a capacity. The trunk capacity itself is `_core/Models/Core Stability.md`; which adaptation axis you're chasing is `_core/Models/Training Adaptations (Galpin 9).md`.

> **This file has been pruned.** Four claims from the original framework were tested and failed; they are **not** stated as model content and are recorded in Falsification so they don't get re-imported. What remains is what survived.

## Mechanism

One causal chain does all the work:

**proximity to failure → recovery cost → ceiling on frequency**, while **motor-control adaptation requires frequency.**

So effort-proximity and frequency are **inversely coupled**. Any goal that needs near-failure effort is frequency-limited; any goal that needs high frequency must stay far from failure. This is why one prescription cannot serve every goal — not because the goals are incompatible, but because **the dose is**.

Three outcome classes, distinguished by where they sit on that trade-off:

| Vector | What you're buying | Effort proximity | Frequency | Fatigue budget | Selection bias |
|---|---|---|---|---|---|
| **LOOK** | muscle size / local volume | **close to failure** | recovery-capped | high | compound + isolation; isolation carries more weight here than elsewhere |
| **PERFORM** | force transfer, bracing, dynamic stability | high **intent**, not to failure | recovery-capped, inside the strength/sport split | high | heavy free-weight compound + anti-movement |
| **FEEL** | positional control, motor competence | **deliberately submaximal** | high, up to daily | near-zero *by design* | controlled / isolated, low load |

Deliberately no ratio percentages or rep brackets — see Falsification #2 and #3.

**Second mechanism, independent of the above:** *how hard you contract and brace under load* moves the outcome more than *which exercise you chose*. Effort spent hunting novel exercises is misallocated; effort spent on intent within a known exercise is not.

### The loading ladder

Sequences a pattern from control toward load. Enter at the step you can own with quality, not the step that looks impressive.

| Step | Stage | Example |
|---|---|---|
| 1 | **Isometric control** — static hold, no load | plank |
| 2 | **Anti-movement + fatigue** — high-rep bodyweight, resist motion | slow dead bugs |
| 3 | **Anti-movement + load** — resist motion against resistance | suitcase carry, DB dead bug |
| 4 | **Movement + fatigue** — dynamic, light, high-rep | cable crunch, contraction-focused |
| 5 | **Movement + load** — heavy dynamic through full ROM | weighted crunch |

Steps 1–3 sit at the FEEL/PERFORM end (control, bracing); 4–5 at the LOOK end (tension, volume). This is a **sequencing heuristic for load tolerance and quality**, not an injury-prevention protocol (Falsification #4).

## Scale of simplicity

The complex object is "hundreds of exercises × load × frequency × individual." This model coarse-grains to **one categorical question — which outcome class is the primary driver? — and returns a dose *class*, not an exercise.** The simplifying move is refusing to reason about the individual movement: fix effort-proximity, frequency and fatigue budget, and the exercise becomes interchangeable within its pattern (exactly why `Exercise Catalog.md` swaps by pattern + adaptation rather than by name).

**Usefulness test:** the payoff exists **only when one primary driver is actually named.** Decline to pick, and the model returns nothing — it relabels the choice instead of collapsing it. It also stops paying off below its scale: it cannot choose between two isolation exercises, or set a precise ratio. Use it for the dose class; use the catalog for the movement.

## Cynefin domain

- **Mechanism — Complicated.** The trade-off is mechanical and derivable: near-failure work costs recovery, recovery caps frequency, control needs frequency. Predictable and repeatable.
- **Outcome — Complex.** Whether a block makes *this* person look how they want, or feel better, is emergent — it competes with energy balance, sleep, stress, prior injury, natural history. **Never lend the trade-off's confidence to the outcome.** This is precisely where the original framework overreached.

## Time horizon (Lyapunov)

- **Dose → adaptation: weeks → a few months.** Predictable; program here.
- **Beyond a block, and for any *outcome* claim at any horizon** → prediction decays. **Stop forecasting, instrument:** re-test each vector on its own metric (LOOK: girth/photos at fixed conditions · PERFORM: 1RM, carry load, jump · FEEL: Sahrmann level, McGill endurance seconds and ratios) on a fixed cadence and steer off measurements.

## Practice

1. **Name the primary driver before selecting anything.** One driver leads per region per block. It sets effort-proximity, frequency and fatigue budget. If it isn't known, establishing it is the first task — not an optional preamble.
2. **Secondary vectors get a maintenance dose, not a competing one.** FEEL costs almost no fatigue, so it can run daily *alongside* LOOK or PERFORM — provided it stays submaximal.
3. **Never take FEEL work near failure.** That converts it into LOOK work and destroys the frequency that makes it work. This is the single most common error the model exists to catch.
4. **Enter the ladder where quality holds.** Earn the loaded steps.
5. **Spend effort on contraction intensity, not novelty.** Same exercise, more intent, beats a new exercise.
6. **Diagnose a stalled program as dose-mismatch first:** daily near-failure work (LOOK dose at FEEL frequency) → accumulating fatigue, no result. Weekly low-load control work (FEEL dose at LOOK frequency) → no adaptation of anything.

## Confidence

- **High** that effort-proximity and frequency are inversely coupled, and that this forbids one dose serving every goal.
- **High** that FEEL-class work must stay submaximal to keep its frequency.
- **Medium** that three buckets are the right carve-up — a useful partition, not a measured one.
- **Medium** on the ladder's ordering as a quality/tolerance progression (mechanically sensible, not trialled).

Nothing in this file rests on a claim graded low — the low-confidence material was removed rather than hedged.

## Falsification

**Prediction if the surviving model holds:** programs that apply one dose profile across incompatible goals underperform matched programs that dose each separately — and specifically, control work driven to failure loses its benefit by losing its frequency.

Four claims from the source framework were tested and **removed**:

1. **"FEEL work reduces low back pain" — failed, removed.** Cochrane (Saragiotto et al. 2016): motor-control exercise **no better than other exercise** for chronic LBP; Smith et al. 2014 concurs; Lederman attacks the isolation premise. **Confound:** most back-pain episodes resolve regardless, so natural history plus the general activity level of people who do daily drills reproduces the pattern. The model now claims only a *trainable capacity* (positional control), never a pain outcome.
2. **Fixed selection ratios (50/50, 75/25, 80/20) — removed as unevidenced.** Expert heuristic; no trial compares 50/50 against 60/40. Replaced by directional "selection bias".
3. **"6–12 reps near failure required for hypertrophy" — failed, removed.** Hypertrophy spans roughly 5–30+ reps when effort is equated; **volume is the driver, load is largely permissive** (Schoenfeld et al.). Replaced by effort-proximity, which is the variable that actually carries the mechanism.
4. **"The ladder protects joints" — unevidenced, removed.** No trial shows step-gating lowers injury risk versus starting light-but-loaded. Retained only as a quality/tolerance sequence.

**Surviving attack, and the honest answer.** The strongest remaining objection is that *"train according to your goal"* is close to tautological, and a tautology is not a model. The rebuttal is that the falsifiable content sits in the **mechanism** (effort-proximity ↔ frequency coupling) and its **prohibition** (Practice §3): the model forbids a specific, popular, concrete behaviour — daily near-failure core work — and that prohibition can be wrong. If control work driven to failure at reduced frequency produced equal control adaptation, the mechanism would be false. It hasn't been tested head-to-head. ❓ **This is the model's weakest joint and the obvious experiment.**

**Verdict — survives, materially narrowed.** After pruning it is a smaller, mechanically-grounded dosing rule rather than a programming framework. Re-checked against the gate: it drives a practice (the goal gate + the prohibition), it is universal, and it remains non-obvious *because* the prohibition contradicts common gym practice. Kept.

## Boundaries & doubts

- **The three buckets are a heuristic partition, not a measured one.** FEEL is not one of Galpin's 9 adaptations — this model and the 9-axis model carve the space differently and must not be mechanically merged.
- **Says nothing about energy balance** — the dominant term for the visible LOOK outcome is body fat, which this model does not address.
- **Weakest in acute pathology.** With disc injury, fracture or radiculopathy, structure dominates and diagnosis outranks any dosing rule (same edge as `Core Stability.md`).
- ❓ Whether FEEL work's near-zero fatigue cost truly holds at daily frequency in someone already training hard, or quietly accumulates.
- ❓ The head-to-head test in Falsification has not been run; the central prohibition is mechanically reasoned, not demonstrated.
