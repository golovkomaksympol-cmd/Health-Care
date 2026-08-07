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

## Step 3 — Signal vs noise: does this measurement resolve the decision?

**Model: `Models/Signal-vs-Noise in Lab Practice.md`. Read it before interpreting any result** — it carries the noise-source taxonomy, the CV/RCV budget table per marker, the arithmetic (CI, RCV, the χ² flat-model test, draws-needed), and the index of individuality. Pull the numbers from there; do not reason about noise from memory and do not restate the model here.

What this step does in a panel workflow:

**Before ordering.** If the expected treatment effect is smaller than the marker's RCV, that marker **cannot** verify the treatment — ordering it is theatre. Check this against the model's budget table while tiering in Step 1, not after the blood is drawn. Prefer low-noise anchors (HbA1c over HOMA-IR) for anything that gates a decision.

**When reading.**

1. Convert each decision-relevant value into **value ± 95% CI** using the model's CV_within. Never report a bare number.
2. Put the **decision threshold on the same line as the CI**:
   - threshold **outside** the CI → the measurement resolved it → **act**;
   - threshold **inside** the CI → **it did not** → do not act on it. In order: take the action safe across the whole interval (usually *change nothing*), repeat under identical conditions and pool, or switch to a lower-noise marker.
3. With **n ≥ 3 draws**, run the flat-model test *before* describing any direction. Three points around a constant almost always look like "rose, then fell".
4. Name explicitly which markers moved beyond noise and which did not. Often only two or three of twenty did — saying so is the main service this step provides.
5. Check **regression to the mean**: if the retest was triggered by a bad value, some of the improvement is artefact, not intervention.

**The override.** RCV governs *"did this change from before?"*, never *"is this value dangerous now?"* An absolute value in a critical range is actionable on a single draw — see Boundaries.

## Step 4 — Confounders: systematic error (bias), not noise

Step 3 handled **random** error, which averages out across draws. This step is **systematic** error: it pushes a result the same direction every time, so repeating the test reproduces the lie instead of cancelling it. No amount of averaging fixes a confounder — you have to know it's there. (The noise model explicitly does **not** cover bias; this table is where it's handled.)

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

Reference ranges and "optimal" targets are different objects answering different questions — **model: `Models/Optimum vs Norm.md`**. Label which one you are quoting, every time, and state the **evidence tier** behind any optimum: a Tier C/D optimum is not more authoritative than the reference range, only differently biased, and must never drive escalating doses without a stop rule. Check the index of individuality before trusting a population range at all. If a previous reading of yours was built on a single noisy draw and later points contradict it, **say so plainly and revise** — a conclusion inherited from a noise peak is worse than no conclusion. Interpretation is for a specific person with a specific history: **surface the decision and its reasoning, don't issue a diagnosis or prescribe.** Anything that changes a prescription goes through their doctor. Red-flag results (severe anemia, glucose in diabetic range, markedly abnormal liver/kidney function, calcium disturbance) → say plainly that this needs prompt medical review, and don't bury it.
