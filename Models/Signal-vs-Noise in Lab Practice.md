# Signal-vs-Noise in Lab Practice

A lab result is **an estimate of a value you cannot see**, not a fact. This model supplies the arithmetic that turns a printed number into an interval, and the one decision rule that follows: **when the decision threshold lies inside the interval, the measurement did not answer the question — do not act on it.** Pure metrology, applied to blood.

Its twin on the target side is [[Models/Optimum vs Norm]]: this model says *how well you know the number*, that one says *what the number should be*.

## Mechanism

You did not measure the person. You measured one tube of their blood, once, on one machine, on one morning:

> **x_observed = μ_true + ε_analytical + ε_pre-analytical + ε_biological**

μ_true is the person's **current homeostatic setpoint** — never directly observed. Interpretation runs the equation backwards: infer a plausible range for μ_true, then ask whether the decision is the same everywhere in it.

**Four independent noise sources stack.** Variances add: **σ_total = √(Σσᵢ²)**.

| Source | What it actually is | Typical size | Controllable? |
|---|---|---|---|
| **Analytical** (CV_a) | Assay imprecision, calibration drift, reagent lot change, analyzer and method differences (HbA1c by HPLC vs immunoassay; LDL calculated vs direct) | 2–7% most chemistry, more for immunoassays | Partly — same lab, same method |
| **Pre-analytical** | Everything between person and analyzer: fasting state, time of day, posture, tourniquet time, hemolysis, delay to centrifugation, tube type, recent exercise / alcohol / stress | **Usually the largest source and the most ignored.** 5–50% | **Yes — the only one you can actually fix** |
| **Within-person biological** (CV_i) | Real oscillation around the setpoint: pulsatile secretion (insulin every 5–15 min; LH/GH/cortisol pulses), circadian rhythm, menstrual phase, season | 2% (HbA1c) to >30% (CRP) | No — only averaging draws reduces it |
| **Between-person biological** (CV_g) | How widely setpoints differ across people | — | Not noise for one person — but it sets the index of individuality below |

**A lab or method switch is bias, not noise.** Noise is random and averages out; a different platform shifts every result the same direction. Never absorb a lab change into a trend silently.

### The arithmetic

**CV_within = √(CV_a² + CV_i²)** · **σ = value × CV_within**

| Question | Formula | Reading |
|---|---|---|
| Where is the true value, from one draw? | **x ± 1.96σ** | 95% CI for μ_true |
| Did two draws really differ? | **RCV = √2 × 1.96 × CV_within** | Change must exceed RCV to be real (√2 — both draws carry error) |
| Is there a trend across n ≥ 3 draws? | **χ² = Σ(xᵢ − x̄)² / σ²**, df = n−1 | Large p → scatter fully explained by noise → flat model stands. For df = 2, **p = e^(−χ²/2)** |
| Best estimate from n draws | **x̄ ± 1.96 σ/√n** | Averaging is the only defence against biological noise |
| Draws needed to pin it to ±δ% | **n ≈ (1.96 × CV_within / δ)²** | Usually a sobering number |

**With n ≥ 3, never read consecutive pairs.** Three draws around a constant will nearly always look like "rose, then fell" — one of them has to be the largest. That shape is the *expected appearance of noise*. Test the whole series against the flat model first; only if flat is rejected does direction mean anything.

### Distributional assumptions — where this arithmetic breaks

Everything above assumes measurement error is **approximately Gaussian on some scale**. That assumption fails in four distinct ways, and **only the first is repairable.**

| # | Failure | Typical markers | Repairable? |
|---|---|---|---|
| 1 | **Right skew (log-normal)** — the common case in biochemistry | ferritin, TG, insulin, CRP, HOMA-IR, most hormones | **Yes — do the arithmetic on the log scale** |
| 2 | **Regime mixture** — the value is drawn from different distributions depending on a latent state, so no single σ exists | CRP in health (0.3–3) vs infection (30–300); ferritin ± inflammation | **No — identify the regime first, then apply within it** |
| 3 | **Censored value** — the result is a bound, not a number | `<0.40`, `>90`, `<0.2` | **No — CI and RCV are undefined. Do not compute them** |
| 4 | **True fat tail** — variance unstable, sample σ does not converge; the extreme observation *is* the signal, not noise to average away | rare in a stable within-person series; real across states | **No — leaves this framework entirely** |

**Case 1 — the log-scale fix (use it by default for skewed markers):**

> σ_log = √(ln(1 + CV_within²)) · **CI = x · e^(±1.96·σ_log)** · **RCV_log = √2 · 1.96 · σ_log**, applied as multiplicative factors e^(±RCV_log)

This yields **asymmetric** limits, and the asymmetry is large enough to flip conclusions:

| CV_within | Naive symmetric RCV | Rise must exceed | Fall must exceed |
|---|---|---|---|
| 10% | ±28% | **+32%** | **−24%** |
| 15% | ±42% | **+51%** | **−34%** |
| 20% | ±55% | **+73%** | **−42%** |
| 25% | ±69% | **+98%** | **−49%** |
| 30% (CRP) | ±83% | **+126%** | **−56%** |

**The naive symmetric test systematically over-calls rises and under-calls falls,** and the error grows with CV. At CV 20%: a +60% rise looks significant symmetrically but is not (needs +73%); a −45% fall looks like noise but is real (needs only −42%). Read a skewed marker symmetrically and you will invent improvements and miss deteriorations — in that order.

**Case 3 — censored values are not small numbers.** `hsCRP <0.40` means "below the quantitation limit", not "0.40" and not "0.2". Substituting a number and computing a CI fabricates precision that does not exist. Treat it as an interval `[0, LoQ)` and reason about the *decision*: if the entire interval sits on one side of the threshold, the measurement resolved the question — which is usually the case at the low end, and is why a censored result is often perfectly actionable even though it is unquantified.

**Two further violations, independent of shape:**

- **CV_a is not constant across the measuring range.** Published analytical CV is a mid-range figure; near the limit of quantitation it degrades badly, often 2–3×. Low-end values are noisier than the table implies.
- **CV_i is interval-dependent, and RCV assumes independent draws.** Population CV_i is typically derived from draws weeks apart. Two draws three days apart are autocorrelated — for slow-drifting markers (ferritin, HbA1c) the real short-interval noise is smaller, and for pulsatile ones (insulin, cortisol) it can be larger. Using one CV_i for every spacing misstates both.
- **Derived quantities inherit and amplify.** HOMA-IR is a *product* of two noisy variables, TG/HDL and fT3/fT4 are *ratios* — errors combine multiplicatively, so these are more skewed than their inputs and belong on the log scale by construction. A ratio whose denominator can approach zero is pathological in the tail and should not be trusted there at all.

### Index of individuality — why "within range" can be meaningless

**II = CV_i / CV_g**

- **II < 0.6** — personal oscillation is narrow next to between-person spread. Population ranges are close to useless: someone can move far from their own setpoint and stay inside the grey bar. True for TSH, creatinine, ferritin, many hormones.
- **II > 1.4** — population ranges work reasonably.

For low-II markers **the person's own previous values are the reference range.** This is the formal justification for tracking a personal baseline instead of the lab's normal band — and the hand-off point to [[Models/Optimum vs Norm]].

### Noise budget

Population priors — **not any individual's own**. Sorted by how far a value must move before the change is real.

| Marker | CV_within | **RCV** | Note |
|---|---|---|---|
| MCV | ~1.8 | **5%** | Trust one value |
| HbA1c | ~2.5 | **7%** | Best low-noise 3-month anchor |
| Calcium | ~2.8 | **8%** | Trust one value |
| HGB | ~3.2 | **9%** | |
| Albumin | ~3.6 | **10%** | |
| Glucose (fasting) | ~5.6 | **15%** | Only if truly fasted |
| Creatinine | ~5.8 | **16%** | |
| Cholesterol | ~6.7 | **19%** | |
| ApoB | ~7.6 | **21%** | |
| fT4 | ~7.8 | **22%** | |
| fT3 | ~9.4 | **26%** | Most "optimal-range" targets sit inside this |
| Vitamin D | ~14 | **39%** | Seasonal confounder on top |
| Ferritin | ~16 | **44%** | Read with CRP |
| TSH | ~20 | **55%** | Plus ±20–50% diurnal |
| TG | ~20 | **57%** | |
| Insulin | ~22 | **60%** | Pulsatile |
| HOMA-IR | ~23 | **64%** | Inherits glucose + insulin error |
| Cortisol | ~26 | **71%** | One random value near-uninterpretable |
| CRP | >30 | **>85%** | Only large moves mean anything |
| Estradiol / FSH / LH | cycle-dominated | — | No stationary setpoint in an irregular cycle — the apparatus below does not apply |

### Regression to the mean

If a test was repeated *because* the first value looked bad, the repeat improves on average **with no intervention at all**. Any "improvement" after acting on an outlier is partly this artefact. It is the single commonest way an intervention gets undeserved credit.

## Scale of simplicity

Twenty numbers, each with a grey bar, several flagged, and a narrative that seems to rise off the page. This model collapses that to **one binary question per marker: does the decision threshold sit inside the interval, or outside it?** The simplifying move is **refusing to interpret the number** and asking instead whether the measurement *resolved the decision*.

**Usefulness test:** it simplifies only when (a) there is a defined decision threshold and (b) a CV prior exists for the analyte. Browsing a panel with no threshold in mind gives the model nothing to collapse. And where the analyte has **no stationary setpoint** — estradiol in an irregular cycle, CRP during infection — there is no μ_true to estimate and the whole apparatus is inapplicable, not merely imprecise.

## Cynefin domain

- **Mechanism — Clear/ordered:** arithmetic on variance components. Deterministic and checkable.
- **Application — Complicated:** picking the right CV prior and spotting which noise source dominates takes expertise, but is knowable.
- **The physiology being measured — Complex.** Never lend the crispness of a confidence interval to confidence about what the biology will do next. A tight CI on today's value says nothing about tomorrow's.

## Time horizon (Lyapunov)

**Effectively zero into the future — this is a nowcast, not a forecast.** The model estimates μ_true *as of the draw*, valid only while the setpoint is stationary (weeks to months under stable conditions). Any intervention, illness, dose change, or life event resets the setpoint, and **pooling draws across a regime change is invalid.** To know the future value there is no substitute for measuring again: the model's own conclusion is *instrument, don't forecast*.

## Practice

**Before ordering (panel design):**
- If the expected treatment effect is **smaller than the marker's RCV**, that marker cannot verify the treatment. Ordering it is theatre. Check this before drawing.
- Prefer low-noise markers as decision anchors (HbA1c over HOMA-IR).

**At the draw — the pre-analytical source is the only large one you control:**
- Morning, 12 h fasted, same time of day, same lab and method as last time; seated 15 min before the draw; no alcohol 72 h; no intense training 48 h; postpone if acutely ill.

**On reading:**
- Report **value ± CI**, never a bare number.
- Put the decision threshold and the CI on the same line. Threshold **outside** CI → act. Threshold **inside** CI → **the measurement did not resolve it; do not act on it.** In order: (1) take the action safe across the whole interval — usually *change nothing*; (2) repeat under identical conditions and pool; (3) switch to a lower-noise marker.
- Never "lean" toward a point estimate inside its own noise band. It carries no directional information.
- With n ≥ 3, run the flat-model test before describing any direction.
- Say out loud which markers moved beyond noise and which did not. Often only 2–3 of twenty did, and naming that is the main service.

**Override — see Boundaries:** an absolute value in a dangerous range is actionable on a single draw regardless of RCV.

## Confidence

- **High** on the arithmetic, the variance-decomposition, and the "threshold inside CI → don't act" rule. This is standard clinical chemistry and metrology.
- **Medium** on the specific CV numbers: they are population priors from biological-variation databases, vary between sources and assays, and are **not** any given person's own.
- **Medium** on the index-of-individuality thresholds (0.6 / 1.4) — conventional cut-points, not hard physics.

## Falsification

**Attempt — the load-bearing claim is "model the noise before acting on a result."** Three serious attacks:

1. **The CVs aren't this person's.** The whole apparatus imports a *population* CV_i to compute *this individual's* interval. Personal biological variation can be materially narrower or wider, so the CI is itself model-dependent — possibly wrong in either direction. → **Qualified:** the interval is a prior-based estimate, not a measured one. For a high-stakes, repeated decision, estimate personal CV from ≥3 draws taken in a stable state and use that instead.

2. **The Gaussian assumption — the sharpest attack on the arithmetic itself.** Most biochemistry is right-skewed, so symmetric ±1.96σ misplaces both limits; at CV 20% the true thresholds are +73% / −42%, not ±55%, which is enough to flip a verdict in either direction. Worse, some markers are not one distribution at all: CRP in health and CRP in infection are different regimes, and a censored `<0.40` is not a number you can put a CI on. → **Partly lands, and splits the model in two.** The skew half is fully repairable — work on the log scale, and the machinery is exact again; this covers most of biochemistry, so "the model only works for Gaussian data" is too strong. The **mixture, censoring and fat-tail halves are not repairable inside this framework** and become hard preconditions: identify the regime, refuse to compute on a bound, and treat a genuine tail observation as signal rather than scatter. See *Distributional assumptions* above.

3. **The strongest attack: it can induce harmful inaction.** Demanding statistical significance before acting will miss real deterioration in exactly the markers with huge RCV. A CRP that doubles is "not significant" at RCV >85%; a ferritin of 5 is one draw. **Statistical non-significance is not clinical irrelevance.** → **This one partly lands, and becomes a hard boundary:** RCV governs *"did this change from before?"*, never *"is this value dangerous now?"* Absolute value in a critical range overrides the entire apparatus.

**Result — survives, qualified.** It genuinely defeats the two commonest interpretation errors (acting on scatter, and narrating a trend out of three points), but only (a) with population CVs flagged as priors, (b) **on the log scale for skewed analytes — the symmetric form is wrong by default in biochemistry**, (c) where a single stationary regime exists at all and the value is not censored, and (d) **with absolute-danger override sitting above it.** Those four qualifiers are the model, not footnotes.

## Boundaries

- **Change-detection only.** Never let RCV suppress action on a dangerous absolute value. Severe anemia, glucose in diabetic range, calcium disturbance, markedly abnormal liver/kidney function → act on one draw, escalate to a clinician.
- **No stationary setpoint → model inapplicable.** Cycle-dependent hormones in irregular cycles, acute-phase reactants during illness. Not "imprecise" — *not defined*.
- **Population CVs are priors**, not this person's values.
- **Gaussian-on-some-scale is a precondition, not a detail.** Right skew → log scale (default for biochemistry). **Regime mixture, censored results (`<LoQ`, `>ULoQ`) and true fat tails are outside the model** — do not compute a CI or RCV for them; establish the regime, or reason directly from the bound and the threshold.
- **Analytical CV degrades near the limit of quantitation** — low-end values are noisier than the budget table shows.
- **RCV assumes independent draws and one fixed spacing.** Short-interval repeats are autocorrelated; the population CV_i does not transfer to every interval.
- **Products and ratios (HOMA-IR, TG/HDL) amplify error multiplicatively** and are log-scale objects by construction.
- **Bias is not covered.** Confounders (iron deficiency raising HbA1c; inflammation raising ferritin; a lab switch) are *systematic* — they survive averaging and this model does not detect them. Handle separately.
- **Pooling across a regime change is invalid** — a new drug, dose, illness or season starts a new series.
- **Silent on whether the marker is worth measuring at all** — that is [[Models/NNT (Number Needed to Treat)]] and the tiering step of the `lab-panel` skill.
- ❓ Personal CV estimation needs ≥3 stable-state draws; how many is genuinely enough for a usable personal prior is unresolved in practice.

## Related

- [[Models/Optimum vs Norm]] — what the target should be, once you know how well you know the number
- [[Models/Scientific Method (Measure Zero)]] — kill before confirm; this model is how "measure" gets error bars
- [[Models/NNT (Number Needed to Treat)]] — the other decision-framing lens: is the intervention worth it at all
- [[Models/Iron Homeostasis]] — ferritin-with-CRP is the worked case of bias, not noise
