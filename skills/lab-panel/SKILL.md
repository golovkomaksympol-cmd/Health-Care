---
name: lab-panel
description: Design a blood-test panel, or interpret one that came back. Use when the user asks which labs to order ("какие анализы сдать", "проверить метаболизм", "what tests should I get", "check my metabolism/thyroid/iron"), asks whether a test is worth doing, or hands over results and asks what they mean. Tiers tests by whether they change an action, treats every result as an estimate of an unseen true value (naming the four sources of noise), refuses to act when noise exceeds signal, and names the confounders that fake a result.
---

# Lab-panel skill

**Language:** reply in the **user's language**, whatever they wrote in. Keep marker names, units and reference ranges in their standard form (ApoB, HbA1c, hsCRP, HOMA-IR, mg/dl, mmol/l) — translating them invites transcription errors on the one thing that must stay exact. This file is written in English; that is not the output language.

Two jobs, same spine: **assemble a panel** (before) and **read it honestly** (after). The spine is `Decision Principles.md` + `Trigger Diagnostics.md` + `meta-thinking.md` (framework root — `_core/` in a health-repo setup, `../../` from this file standalone).

**The one rule everything else serves:** a test earns its place only if its result would **change an action**. Everything else is anxiety with a co-pay.

**Its metrological twin:** a result is an *estimate of a value you cannot see*, carrying uncertainty. When the uncertainty is wider than the decision, the correct move is to **not decide** — see Step 3.

## Step 0 — What is the actual question?

Don't produce a panel from a topic word. Pin down:
- **Goal** — screening a healthy person / chasing a symptom / monitoring a known condition / checking a drug's effect or safety.
- **Baseline** — what's already been measured, when, and at which lab. **Never re-order something inert that's already known** (see the once-in-a-lifetime list below).
- **What's on board** — drugs and supplements. These both *change* results and *are the reason* for some tests.
- **Constraints** — budget, lab availability, needle-fatigue, how far they'll travel. Friction is a real constraint: a perfect panel at an unreachable lab scores zero.

If the ask is vague ("check everything"), narrow it to 1–3 systems. A shotgun panel guarantees an incidental finding that costs more worry than it resolves.

## Step 1 — Tier every candidate test

For each one, ask out loud:

> **"If this comes back high, what do I do? If it comes back normal, what do I do?"**
> Same answer to both → **drop it.**

| Tier | Meaning |
|---|---|
| **1 — Core** | Directly gates a decision *this cycle*. Order it. |
| **2 — Context** | Doesn't decide alone, but needed to interpret a Tier 1 result (e.g. ferritin next to HbA1c; CRP next to ferritin). Order it. |
| **3 — Trigger-only** | Order **only if** a specific finding fires — see `Trigger Diagnostics.md`. Name the trigger; don't pre-order. |
| **Don't** | No action follows, or it's inert and already known. Say why you're excluding it — the exclusions are half the value. |

**Measure once, then never again** (unless the clinical picture changes): Lp(a), genetics/pharmacogenetics, ApoA1, coeliac genetics. **Inert on a 3-month cadence:** anti-TPO, DHEA-S. Re-testing these is noise with a fee.

## Step 2 — The metabolic panel (the most-asked case)

"Check my metabolism" means: *is insulin resistance developing, are lipids atherogenic, is the liver taking damage, is there smouldering inflammation?* Glucose alone answers none of it — **glucose is the last thing to break**, often a decade after the trouble starts.

**Tier 1 — core**

| Test | Why it's here, not something else |
|---|---|
| **Fasting glucose + fasting insulin → HOMA-IR** | Insulin rises for years while glucose stays normal. HOMA-IR (= glucose × insulin / constant) sees the compensation. Cheap, and the earliest mover. |
| **HbA1c** | ~3-month integrated glycemia. **Low biological noise** — the best single anchor for a 3-month decision (contrast HOMA-IR, which is noisy; see Step 3). |
| **ApoB** | The causal atherogenic particle count. Superior to LDL-C, which mis-ranks risk at high TG or small dense particles. If you order one lipid number, this is it. |
| **Full lipid panel** (total, HDL, LDL, TG, non-HDL) | non-HDL and TG carry the metabolic signal; enables the free ratios below. |
| **ALT, AST, GGT** | Metabolic (fatty) liver disease is the liver face of insulin resistance, and it's silent. GGT also flags alcohol. |
| **hsCRP** | Low-grade systemic inflammation — an independent cardiometabolic risk channel. Must be read outside acute illness. |
| **Uric acid** | Tracks fructose load and insulin resistance; independently linked to hypertension. |
| **TSH** | Thyroid dysfunction masquerades as "slow metabolism" and shifts lipids. One test rules it in or out. |

**Free — computed, no extra blood.** Always calculate these; people pay for panels and then leave the best signal on the table:
- **TG/HDL ratio** — strong insulin-resistance proxy (same units).
- **TyG index** = ln(fasting TG × fasting glucose / 2) — outperforms HOMA-IR in several cohorts.
- **non-HDL** = total − HDL. **HOMA-IR** from the two values above.

**Tier 2 — context (order alongside, or you'll misread Tier 1)**
- **Ferritin (+ CRP to interpret it)** — see the HbA1c trap in Step 4. Also the commonest fixable cause of fatigue that gets blamed on "metabolism".
- **Creatinine → eGFR**, electrolytes — baseline organ function, and required before several drugs.
- **Vitamin D (25-OH)** — only if it will actually be dosed and re-checked.

**Tier 3 — trigger-only:** fasting C-peptide, OGTT, Lp(a) *(once, ever)*, thyroid antibodies, liver elastography/FIB-4, CK, PTH. Each has its trigger in `Trigger Diagnostics.md`.

**Don't order for metabolic screening:** insulin *without* glucose (uninterpretable), "toxin"/food-sensitivity IgG panels, hair mineral analysis, tumour markers in an asymptomatic person, or a repeat of anything in the once-ever list.

> Other systems: build the same way — Tier 1 = what decides, Tier 2 = what makes Tier 1 readable, Tier 3 = gated by `Trigger Diagnostics.md`.

## Step 3 — Metrology: you are estimating a value you cannot see

This is the step people skip, and it is the one that decides whether drawing the blood was worth it.

**What a result actually is.** You did not measure the person. You measured one tube of their blood, once, on one machine, on one morning. What you want is **μ — their current true setpoint** for that analyte. What you get is:

> **x_observed = μ_true + ε_analytical + ε_pre-analytical + ε_biological**

Interpretation means running that backwards: from the number on the page, infer a **range** that plausibly contains μ_true — then ask whether the decision is the same everywhere in that range. If yes, act. If no, the measurement did not answer the question, however precise the printout looks.

**This is metrology, not medicine.** A measurement carries no information unless its uncertainty comes with it. `fT3 = 2.52` is not a fact. `fT3 = 2.52 ± 0.47 (95% CI)` is.

### 3a. Where the noise comes from — name the sources, don't just quote a CV

Four independent sources stack. Variances add, so **σ_total = √(Σσᵢ²)**. Most people account for the first and get ambushed by the second.

| Source | What it actually is | Typical size | Controllable? |
|---|---|---|---|
| **Analytical** (CV_a) | Assay imprecision, calibration drift, reagent lot change, analyzer differences, method differences (HbA1c by HPLC vs immunoassay; LDL calculated vs direct) | 2–7% most chemistry; more for immunoassays | Partly — same lab, same method |
| **Pre-analytical** | Everything between the person and the analyzer: fasting state, time of day, posture, tourniquet time, hemolysis, delay to centrifugation, tube type, recent exercise / alcohol / stress | **Usually the largest single source, and the most ignored.** 5–50% depending on analyte | **Yes — this is the one you can actually fix** (Step 5) |
| **Within-person biological** (CV_i) | Genuine physiological oscillation around the setpoint: pulsatile secretion (insulin every 5–15 min; LH/GH/cortisol pulses), circadian rhythm, menstrual phase, season | 2% (HbA1c) to >30% (CRP) | No — irreducible. Only averaging draws reduces it |
| **Between-person biological** (CV_g) | How widely setpoints differ across people | — | Not noise for one person — but see 3c |

**A lab switch is not noise, it is bias.** Noise is random and averages out; a different platform or method shifts every result the same way. Never absorb a lab change into a trend silently — re-baseline, or state that the comparison isn't clean.

### 3b. The arithmetic

**CV_within = √(CV_a² + CV_i²)** · **σ = value × CV_within**

| Question | Formula | Read as |
|---|---|---|
| Where is the true value, from one draw? | **x ± 1.96σ** | 95% CI for μ_true |
| Did two draws really differ? | **RCV = √2 × 1.96 × CV_within** | Change must exceed RCV to be real (√2 — both draws carry error) |
| Is there a trend across n ≥ 3 draws? | **χ² = Σ(xᵢ − x̄)² / σ²**, df = n−1 | Large p → scatter fully explained by noise → **flat model stands** |
| Best estimate from n draws | **x̄ ± 1.96 σ/√n** | Averaging is the only way to beat biological noise |
| How many draws to pin it to ±δ%? | **n ≈ (1.96 × CV_within / δ)²** | Often a sobering number |

For df = 2 (three draws) the p-value has a closed form: **p = e^(−χ²/2)**.

**With three or more points, never read consecutive pairs.** Three random draws around a constant will nearly always look like "rose, then fell" — one of them has to be the largest. That shape is the *expected appearance of noise*, not a turning point. Test the whole series against the flat model first; only if flat is rejected do you tell a story about direction.

> **Worked example.** fT3 measured three times: 2.65 → 3.01 → 2.52 (CV_within 9.4%). Mean 2.73. Predicted σ = 2.73 × 0.094 = 0.257; **observed SD = 0.254** — the scatter *is* the predicted noise, to two figures. χ² = 1.95, df = 2, **p = 0.38** → flat model not rejected. Best estimate **2.73, 95% CI [2.44–3.02]**. The apparent rise-and-fall was nothing. And to pin that same fT3 to ±5% would need n ≈ 14 draws — so "hit an optimal fT3 of exactly 3.0" is not a reachable target by blood draw.

### 3c. Index of individuality — why "within range" can be meaningless

**II = CV_i / CV_g**

- **II < 0.6** — the person's own oscillation is narrow next to how much people differ. Population reference ranges are close to useless: someone can move far from their own setpoint and still sit comfortably inside the grey bar. True for TSH, creatinine, ferritin, many hormones.
- **II > 1.4** — population ranges work reasonably.

For low-II markers, **the person's own previous values are the reference range.** This is the entire justification for tracking a personal baseline instead of chasing the lab's normal band.

### 3d. Noise budget by marker

CV_within and RCV (%), sorted by how far a value must move before the change is real. Population priors — **not this person's own**; say so when you use them.

| Marker | CV_within | **RCV** | Practical meaning |
|---|---|---|---|
| MCV | ~1.8 | **5%** | Trust a single value |
| HbA1c | ~2.5 | **7%** | Best low-noise anchor for a 3-month decision |
| Calcium | ~2.8 | **8%** | Trust a single value |
| HGB | ~3.2 | **9%** | |
| Albumin | ~3.6 | **10%** | |
| Glucose (fasting) | ~5.6 | **15%** | Only if truly fasted |
| Creatinine | ~5.8 | **16%** | |
| Cholesterol | ~6.7 | **19%** | |
| ApoB | ~7.6 | **21%** | |
| fT4 | ~7.8 | **22%** | |
| fT3 | ~9.4 | **26%** | An "optimal-range" target usually sits inside this |
| Vitamin D | ~14 | **39%** | Also seasonal — a confounder on top |
| Ferritin | ~16 | **44%** | Read with CRP |
| TSH | ~20 | **55%** | Plus ±20–50% diurnal — same time of morning, always |
| TG | ~20 | **57%** | |
| Insulin | ~22 | **60%** | Pulsatile; never decide on one draw |
| HOMA-IR | ~23 | **64%** | Inherits both glucose and insulin error |
| Cortisol | ~26 | **71%** | One random value is near-uninterpretable |
| CRP | >30 | **>85%** | Only large moves mean anything |
| Estradiol / FSH / LH | cycle-dominated | — | Meaningless without cycle phase; in irregular cycles, near-uninterpretable as a single point |

### 3e. The decision rule — if noise ≥ signal, do not act

Put the decision threshold and the confidence interval on the same line:

- Threshold **outside** the CI → the measurement resolved it. **Act.**
- Threshold **inside** the CI → the measurement did **not** resolve it. **Do not act on it.** In order of preference: (1) take the action that is safe across the whole interval — usually *change nothing*; (2) repeat under identical conditions and pool; (3) switch to a lower-noise marker answering the same question (HbA1c instead of HOMA-IR).

Never "lean" toward the point estimate inside its own noise band — a number there carries no directional information. Example: HOMA-IR 2.0 → 1.5 looks like a 25% improvement, but RCV is ~64%. Statistically the two are the same number. Say so, rather than starting or stopping a drug on it.

**Feed this back into Step 1, before drawing:** if the expected treatment effect is smaller than the marker's RCV, that marker **cannot** verify the treatment. Ordering it is theatre. Check this when designing the panel, not when reading it.

## Step 4 — Confounders: systematic error (bias), not noise

Step 3 handled **random** error — it averages out across draws. This step is **systematic** error: it pushes a result the same direction every time, so repeating the test reproduces the lie instead of cancelling it. No amount of averaging fixes a confounder; you have to know it's there.

Check these *before* interpreting, and *before* crediting an intervention:

| Confounder | Effect | What to do |
|---|---|---|
| **Iron deficiency ↑ HbA1c** | Falsely raises it; correcting iron lowers HbA1c with glycemia unchanged | Always read HbA1c **beside ferritin**. Don't credit the drop to diet. |
| **Inflammation / infection ↑ ferritin** | Acute-phase reactant — masks true depletion | Never read ferritin without CRP. Postpone if acutely ill. |
| **Recent bleeding ↓ ferritin, ↓ HGB** | Real but transient | Wait ≥1 week after bleeding stops. |
| **Non-fasting / recent meal ↑ TG, insulin, glucose** | Large | 12 h fast for anything metabolic. |
| **Alcohol ↑ TG, GGT** | 1–3 days | No alcohol 72 h before. |
| **Hard exercise ↑ CK, ALT/AST** | Days | No intense training 48 h before. |
| **Iron supplements ↑ serum iron / TSAT** | 2–4× for hours | Hold 24–48 h (a week for clean TSAT). **Ferritin and HbA1c are unaffected — do NOT stop iron for those.** |
| **TSH diurnal swing** | ±20–50%, peaks overnight, troughs mid-afternoon | Always same time of morning. |
| **Posture / dehydration ↑ HGB, HCT** | 5–10% | Seated 15 min before the draw. |
| **Biotin supplements** | Skews many immunoassays (thyroid, troponin) | Stop 2–3 days before. |
| **Statin / drug started or changed** | The point of the test — but timing matters | Lipids plateau at 4–6 weeks; test after that, not before. |
| **Lab / method switch** | Shifts absolute values | Same lab for trends. Note it when comparing across labs. |

**Adherence before escalation.** If a drug-monitored marker worsens, check whether the drug was actually taken *before* concluding the dose is too low. Escalating an unswallowed drug fixes nothing.

## Step 5 — Prep protocol (state it with every panel)

Morning draw, **12 h fasted** (water fine) · **no alcohol 72 h** · **no intense training 48 h** · seated 15 min before the draw · same lab as last time · chronic meds **after** the draw unless the test is about drug level/effect · postpone if acutely ill or recently bleeding · note cycle day for sex hormones (and skip luteal progesterone if cycles are irregular — untimeable, so it's noise).

## Step 6 — Cost & logistics

- **Packages vs individual:** labs bundle. Price the bundle against the à-la-carte set — bundles often win even carrying tests you didn't ask for. Never let a bundle's freebies become new anxiety.
- **One draw, not three.** Batch everything into a single visit; a test that needs a special lab is a *separate decision* — is it worth the trip? Often a cheap widely-available sentinel gates it (normal calcium closes the PTH question).
- Show a total and, if it's over budget, a **trim list ranked by what you lose** — never silently drop tests.

## Output format

**Designing a panel:**
1. One line: the question this panel answers.
2. **Tier 1 / Tier 2** table — test → what decision it drives.
3. **Tier 3** with each trigger named.
4. **Explicitly excluded** + why (this is signal, not filler).
5. Prep protocol + cost/logistics.
6. The noise caveat: which results won't be trustworthy on a single draw, and — for any marker meant to verify an intervention — whether the expected effect even exceeds its RCV.

**Interpreting results:**
1. Lead with **what changes** — the 1–3 numbers that alter a decision.
2. For each: value, **95% CI for the true value**, direction vs last time, and **whether the change exceeds RCV** (real) or not (noise). State the CI, not just the point.
3. With **n ≥ 3 draws**: test the series against the flat model (χ²) before describing any direction; report the pooled estimate and its CI.
4. Say explicitly which markers moved beyond noise and which did not — often only 2–3 of twenty did, and naming that is the main service.
5. Confounder check (Step 4) *before* conclusions.
6. Free computed ratios.
7. Then the normal/unremarkable, briefly.
8. Actions — and for every threshold, whether the CI actually cleared it. If not, say the measurement did not resolve it and act accordingly.
9. Trigger and date for the next test.

## Boundaries

Reference ranges are **population** ranges, and "optimal" targets are a separate, often stricter claim — label which you're using, and check the index of individuality (3c) before trusting a population range at all. If a previous reading of yours was built on a single noisy draw and later points contradict it, **say so plainly and revise** — a conclusion inherited from a noise peak is worse than no conclusion. Interpretation is for a specific person with a specific history: **surface the decision and its reasoning, don't issue a diagnosis or prescribe.** Anything that changes a prescription goes through their doctor. Red-flag results (severe anemia, glucose in diabetic range, markedly abnormal liver/kidney function, calcium disturbance) → say plainly that this needs prompt medical review, and don't bury it.
