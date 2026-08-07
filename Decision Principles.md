# Decision Principles

How to choose interventions when reasoning about a patient's care.

## Optimal > Normal

Lab "reference ranges" are population averages — built from a sampled population, so where that population is unhealthy the range encodes the disease as normal. Aim for **outcome-anchored optimal targets** with a margin of safety, not just "within normal".

**But grade the optimum before chasing it.** An optimum backed by RCT + Mendelian randomization (ApoB) outranks the reference range; an optimum from observational data or a "functional range" does not — it is just differently biased, and chasing it with a fixed escalating dose is how overtreatment happens. Full model incl. evidence tiers and failure modes: `_core/Models/Optimum vs Norm.md`. A target is also useless if it is narrower than the marker's measurement noise — `_core/Models/Signal-vs-Noise in Lab Practice.md`.

## Input-driven control

Manage **inputs** (sleep, training, nutrition, supplements) — not lagging biomarkers. Inputs are controllable in real time; biomarkers are quarterly delayed feedback. Building the system on inputs makes adherence the metric of interest.

## Signal-to-noise

Prefer tests that **change actions**. If a result wouldn't change the protocol, the test generates anxiety, not information. Skip it.

Examples of low-signal tests for asymptomatic patients: AFP (without cirrhosis/hepatitis), CA-19-9, CA-15-3, CEA, ApoA1, full-body PET-CT, 17-OH Progesterone in adults without childhood symptoms.

## Hierarchy of controls

Eliminate root causes before patching with PPE/meds.

- Root cause (lifestyle, environment, diet) > symptom suppression.
- Causal upstream marker (ApoB, fasting insulin) > derivative marker (total cholesterol, fasting glucose alone).
- Continuous monitoring (CGM, HRV) > spot check.

## Constraint satisfaction (global > local optimum)

The body is a constraint-satisfaction problem. Optimizing one number at the expense of others is a loss.

- Lipid optimization must not crater hormones.
- Iron supplementation must not raise blood viscosity beyond safe limits.
- HIIT progression must not destroy sleep architecture.

Always check what a new intervention costs the rest of the system before adopting it.

## Adherence first

"80% done for years" beats "perfect, then abandoned." Pick the version of the protocol the patient will actually run.

This is why protocols in `Practices Framework.md` have explicit Decay Rate (forgiveness for missed days) — high-adherence-tolerance practices are preferred when designing the stack.

## Antifragility

Dose stressors intentionally — cold, fasting, heavy weights, hard intervals — so the system adapts. Excess **avoidance of stress** is itself a risk factor at every age.

## Tail-risk hedging

Avoid risk of ruin even at moderate cost. Insure low-probability, high-cost failures with screening and genetics-informed decisions.

- Thrombophilia panel before HRT if obstetric history hints at risk.
- CAC score when ApoB elevated, before deciding on lifelong statin.
- Colonoscopy at 45 (not 50) when family or symptom hints exist.
- Lp(a) once in a lifetime — if high, it changes the calculus on everything downstream.

## Models: map ≠ territory

Reason from explicit models — but every model is a *partial* map. A working model always states **Mechanism / Practice / Confidence / Boundaries**; a model without stated limits gets misapplied beyond where it holds. Build a model only when it's a **live constraint or changes a decision** — don't manufacture speculative taxonomies or thin container files (a principle, a cross-link, or a `❓` stub beats a hollow model). Prefer a **minimally-correct model of sufficient accuracy** over a perfect unfinished one (Munger).

Meta-model (format + when to write / not write a model): `_core/Models/AGENT.md`.

## When two principles conflict

Hierarchy when in tension:
1. **Tail-risk hedging** (avoid ruin)
2. **Constraint satisfaction** (don't break other systems)
3. **Hierarchy of controls** (treat root, not symptom)
4. **Adherence first** (a plan only counts if it runs)
5. **Optimal > Normal** (everything else equal, push toward optimum)
