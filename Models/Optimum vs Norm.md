# Optimum vs Norm

Two different bars get quoted against the same lab number, and they answer different questions. **The reference range asks "are you unusual?" The optimal target asks "are you likely to do well?"** Confusing them runs in both directions — accepting disease as normal, *and* chasing a target that was never earned. This model is about knowing which bar you are quoting and what evidence stands behind it.

Its twin is [[Models/Signal-vs-Noise in Lab Practice]]: that model says *how well you know the number*, this one says *what the number should be*. Neither is usable without the other.

## Mechanism

### How a reference range is actually built

1. Assemble a **reference population** — often blood donors, or simply people who came to the lab and were not obviously ill.
2. Take the **central 95%** (2.5th–97.5th percentile, or mean ± 1.96 SD).
3. Print it as the grey bar.

Three consequences follow **by construction**, not by accident:

- **5% of perfectly healthy people fall outside it.** "Abnormal" is partly a definition, not a finding.
- **The range describes the sampled population, not health.** Where that population is metabolically unhealthy — most modern ones — the range **encodes the prevailing disease as normal**. Fasting glucose "normal to 99" and HbA1c "normal to 5.9%" are the canonical examples: both sit well inside the range where cardiometabolic risk is already rising.
- **It is lab- and method-specific**, and where it is partitioned by age it can bake age-related decline in as "normal for you".

### How an optimal target is built

From **outcome data** — the value at which a hard endpoint (event, mortality, function) is minimized. This is a different epistemic object, and its quality varies enormously.

**The half people skip: optima have their own failure modes.**

| Failure mode | What goes wrong | Example shape |
|---|---|---|
| **Observational confounding** | Low X associates with good outcomes ≠ lowering X helps. Reverse causation is rampant | Low cholesterol in the frail elderly tracks illness, not benefit |
| **U-shaped curve** | Both extremes harm; a "lower/higher is better" heuristic overshoots the bottom of the U | Sodium, TSH, vitamin D |
| **Which outcome?** | Optimal for CVD may differ from optimal for cancer, bone, or cognition. Single-outcome optimization is local optimization | Aggressive lipid targets vs hormone/steroid substrate |
| **Unreachable through noise** | The optimal band is narrower than the marker's RCV, so you cannot steer to it | fT3 "3.0–4.0" against RCV ~26% — see [[Models/Signal-vs-Noise in Lab Practice]] |

### Evidence tiers behind an optimum

This is the operative part. Not all optima are equal, and treating them as equal is the error.

| Tier | Basis | Weight |
|---|---|---|
| **A** | RCT **and** Mendelian randomization agree, monotonic dose-response across the range | Strong. Outranks the reference range outright |
| **B** | RCT in a defined population, or consistent MR alone | Good, within the trial's population and horizon |
| **C** | Observational association, dose-response plausible, no causal test | Weak. **Not more authoritative than the reference range — just differently biased** |
| **D** | Expert consensus, mechanism, or "functional range" with no outcome data | Not an optimum. It is an opinion with a number attached |

**ApoB is Tier A** — MR and RCT both show lower-is-better, monotonic, causal ([[Models/ApoB and Atherosclerosis]]). "Optimal ApoB" is on far firmer ground than the reference range.
**"Optimal fT3 3.0–4.0" or "optimal vitamin D 50–70 for autoimmunity" is Tier C at best** — observational, U-shape plausible, no causal test. Chasing it with a fixed dose and no monitoring is how a healthy person is overtreated into a toxic level.

## Scale of simplicity

"What should this number be?" invites an argument about medical philosophy. This model collapses it to **two questions with checkable answers: which bar am I quoting, and what tier is the evidence behind the optimum?** That is tractable at the bedside in under a minute.

**Usefulness test:** it simplifies only where **outcome data exists**. Where there is none, there *is* no optimum — only the reference range and someone's preference. Naming a "functional optimum" absent outcome data does not make the decision simpler, it fakes precision. Drop the model and say the target is unknown.

## Cynefin domain

- **Mechanism (how ranges and targets are constructed) — Clear/ordered:** statistics and study design, fully checkable.
- **Choosing a target for a person — Complicated at best, Complex in the multi-outcome case:** trading a lipid optimum against a hormone optimum against quality of life has no closed-form answer, and the right call is visible mainly in hindsight. **Never lend Tier-A confidence about one endpoint to whole-organism "optimization."**

## Time horizon (Lyapunov)

Both bars move, on different clocks:
- **Reference ranges shift over decades** as the sampled population changes — usually in the unhealthy direction.
- **Optimal targets shift over years** as trials report; several have moved substantially within a career.

Neither is a constant of nature. **Re-check the provenance of any target every few years; never hard-code one into a protocol without its date and tier.**

## Practice

- **Label which bar you are quoting, every time.** "Within the reference range" and "at target" are different statements. Writing them interchangeably is the root error.
- **Ask for the tier before adopting an optimum.** Tier A/B → treat as the real target. Tier C/D → treat as a hypothesis; do not chase it with escalating doses.
- **Check the index of individuality first.** For low-II markers (TSH, creatinine, ferritin) the population range is nearly uninformative — the person's own prior values are the reference. See [[Models/Signal-vs-Noise in Lab Practice]].
- **Check the optimum against the noise floor.** If the target band is narrower than the marker's RCV, it is not steerable. Widen the target or pick a different marker; do not titrate into noise.
- **Assume a U unless the dose-response says otherwise.** For any Tier C/D optimum, "more is better" is an assumption, not a finding. Escalate with monitoring, never with a fixed dose held indefinitely.
- **"Everything is normal" is not the end of a conversation** — ask which values, and where they sit relative to an outcome-anchored target.
- **Symmetrically: "not at optimum" is not a diagnosis.** A Tier C optimum missed by a noise-width is not a finding at all.

## Confidence

- **High** that reference ranges are population-descriptive by construction and encode prevailing disease — this is definitional.
- **High** that optima vary enormously in evidential quality and that treating them as interchangeable causes overtreatment.
- **Medium** on the tier boundaries as drawn here — a working taxonomy, not a standard.
- **Low/varies** on any specific optimal number; each must be checked separately for its own tier and date.

## Falsification

**Attempt — the load-bearing claim is "prefer an outcome-anchored optimum over the population reference range."** The strongest attack:

> **"An optimum is just a norm derived from a different, cherry-picked population. You have replaced one arbitrary bar with another and added overtreatment risk."**

This attack **largely lands** for Tier C/D targets. Observational optima inherit confounding, healthy-user effects and reverse causation; "functional ranges" often trace to a single lab's marketing or one author's book. Acting on them produces real harm: supplement overshoot, unnecessary drugs, and a patient anxious about a number nobody has shown matters. A concrete failure shape: chasing a Tier-C "optimal" vitamin D band with a fixed high dose and no interim measurement overshoots into the potentially toxic range, while the boring reference range would have kept the person safe.

Where it **fails to land** is Tier A. When MR and RCT agree with a monotonic dose-response — ApoB being the clean case — the causal claim does not depend on the sampled population at all, and the optimum genuinely outranks the reference range.

**Result — survives, but inverted from the naive form.** The model is *not* "optimum beats norm." It is: **know which bar you are quoting, and know its tier. A Tier-C optimum is not more authoritative than the reference range — only differently biased.** That inversion is the whole value; without it, "Medicine 3.0" degrades into confident overtreatment against numbers nobody validated.

## Boundaries

- **No outcome data → no optimum.** Say the target is unknown rather than inventing a functional range.
- **Tier C/D optima must not drive escalating doses** without interim measurement and a stop rule.
- **Says nothing about measurement uncertainty** — a target is useless if unreachable through noise. Pair with [[Models/Signal-vs-Noise in Lab Practice]] every time.
- **Multi-outcome trade-offs are outside it.** The model picks a target for one endpoint; it cannot rank endpoints against each other.
- **Population transportability:** an optimum from one population (age, sex, ancestry, risk stratum) may not transport. Check whose trial it was.
- **Silent on cost, burden and adherence** — a slightly worse target reliably hit beats a better one abandoned.
- ❓ The tier taxonomy here is a working construct; there is no agreed standard for grading "optimal" biomarker targets, which is itself part of the problem.

## Related

- [[Models/Signal-vs-Noise in Lab Practice]] — how well you know the number; supplies the noise floor a target must clear
- [[Models/ApoB and Atherosclerosis]] — the Tier-A worked example
- [[Models/NNT (Number Needed to Treat)]] — converts "hitting the target" into absolute benefit
- [[Models/Scientific Method (Measure Zero)]] — kill before confirm; the discipline behind tiering
