# NNT — Number Needed to Treat

The single honest number for **"is this treatment worth it?"** — how many people must receive a treatment for **one extra** to get the benefit. A decision/communication lens, applied on top of any intervention model (statins, probiotics, screening, supplements). Its twin is **NNH — Number Needed to Harm.**

## Mechanism

- **NNT = 1 / ARR**, where **ARR (absolute risk reduction) = control event rate − treated event rate.** It is the reciprocal of the *absolute* benefit.
- **Its whole power is forcing absolute, not relative, risk.** Relative risk reduction (RRR) is the number marketing quotes and it is scale-free — it hides baseline risk:
  - "Cuts risk 50%" off a **2% → 1%** baseline: ARR 1% → **NNT 100.**
  - "Cuts risk 50%" off a **40% → 20%** baseline: ARR 20% → **NNT 5.**
  - **Identical RRR, 20× different real value.** NNT exposes exactly what RRR conceals.
- **NNT is not a property of the drug** — it depends on **baseline risk** and **time horizon.** The same drug has a low NNT in a high-risk person and a high NNT in a low-risk one.
- **Value ≈ NNT weighed against NNH** (same arithmetic on the harm side: NNH = 1 / absolute risk increase of harm), each scaled by how bad the outcome/harm is.

## Scale of simplicity

"Is this treatment worth it?" is a tangle — RRR, p-values, hazard ratios, confidence intervals, mechanism plausibility. This model collapses all of it to **one integer a patient and clinician can both hold: treat N, one benefits.** The simplifying move is **refusing the relative/p-value scale** as the place you decide, and dropping to the **absolute, per-person integer** you can weigh directly against harm, cost, and hassle.

**Usefulness test:** NNT only simplifies when there's a **single discrete outcome over a defined horizon in a population like yours.** If the outcome is continuous, the horizon undefined, or your baseline unlike the trial's, NNT stops making the decision simple — that's below/outside its scale (see Boundaries), and forcing it there fakes precision.

## Cynefin domain

- **Mechanism — Clear/ordered:** it's arithmetic. Deterministic, checkable.
- **Outcome — Complex/irreducibly stochastic:** NNT is a **population frequency; it cannot tell you whether *you* are the 1 or the (N−1).** You never learn if you were the responder. Do not read a population NNT as a personal probability of *your* benefit beyond the base rate.

## Time horizon (Lyapunov)

NNT is **meaningless without its time window** — "NNT 50" over 5 years ≠ over 1 year. It's welded to the trial's follow-up. **Extrapolating past the trial horizon is invalid** → recompute as horizon and baseline risk change; don't forecast an NNT the data didn't measure.

## Practice

- **Always convert RRR → ARR → NNT before deciding.** Refuse any claim quoted only as relative ("halves your risk") until you know: *off what baseline, over what time, what's the NNT?*
- **Recompute for YOUR baseline risk** — a low-risk person's personal NNT is *higher* (worse) than the trial average; a high-risk person's is lower (better). This is how "targeted, not reflexive" gets its math.
- **Pair NNT with NNH** and with the **severity** of what's prevented vs. caused. NNT 100 to prevent death can beat NNT 5 to prevent a mild rash.
- **Red flag:** a treatment sold on relative risk reduction alone — that's the tell that the absolute benefit is small.

## Confidence

- **High:** the arithmetic and the RRR-deception point — bedrock evidence-based medicine.
- **Caveat (Medium):** trial NNTs transport imperfectly to an individual (baseline risk, adherence, comorbidity differ), and NNT's statistical behaviour is awkward (below).

## Falsification

**Attempt — the load-bearing claim is "NNT is the honest single number for treatment value."** Three serious attacks:

1. **It reifies a binary that may not exist.** NNT assumes "1 person fully saved, N−1 get nothing." For **continuous outcomes** (everyone's blood pressure drops a little) that's a fiction — benefit is shared, not lumped into 1-in-N. → **Qualified:** NNT is valid for **discrete event outcomes** (event / no event over a horizon), misleading for continuous ones.
2. **It has poor statistical properties.** When the effect is non-significant, the **confidence interval of NNT is discontinuous** — it runs from NNT-benefit *through infinity* to NNT-harm (Altman, Hutton). You can't naively average or meta-analyse NNTs. → **Qualified:** NNT is a **communication/decision-framing tool, not an analysis statistic.** Compute effects in ARR/RR with proper CIs; convert to NNT only for the final framing.
3. **NNT alone isn't "value."** Without **NNH, outcome severity, cost, and QoL** it's one axis of several. → **Qualified:** necessary, not sufficient.

**Result — survives, qualified.** It genuinely defeats relative-risk deception and gives a per-person scale everyone can reason about — but only (a) for **discrete outcomes over a fixed horizon**, (b) after **recomputing for the individual's baseline risk**, (c) **paired with NNH + severity**, and (d) used as **framing, not a meta-analytic summary.** And it **never identifies who the 1 is.** Those four qualifiers are the model, not footnotes.

## Boundaries

- **Needs a defined outcome + time horizon + comparable baseline population** — absent any of these it's not interpretable.
- **Continuous outcomes → NNT misleads** (use mean difference instead).
- **Silent on severity and harm** — always read alongside *what* is prevented and NNH.
- **Population statistic — silent on the individual;** cannot identify responders.
- **Trial NNT ≠ your NNT** (baseline risk, adherence, comorbidity, real-world vs. RCT conditions).
- **Awkward CIs** — treat as communication, not as a quantity to pool.