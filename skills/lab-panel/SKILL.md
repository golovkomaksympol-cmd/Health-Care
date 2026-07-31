---
name: lab-panel
description: Design a blood-test panel, or interpret one that came back. Use when the user asks which labs to order ("какие анализы сдать", "проверить метаболизм", "what tests should I get", "check my metabolism/thyroid/iron"), asks whether a test is worth doing, or hands over results and asks what they mean. Tiers tests by whether they change an action, models measurement noise before declaring a trend, and names the confounders that fake a result.
---

# Lab-panel skill

Two jobs, same spine: **assemble a panel** (before) and **read it honestly** (after). The spine is `Decision Principles.md` + `Trigger Diagnostics.md` + `meta-thinking.md` (framework root — `_core/` in a health-repo setup, `../../` from this file standalone).

**The one rule everything else serves:** a test earns its place only if its result would **change an action**. Everything else is anxiety with a co-pay.

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

## Step 3 — Model the noise BEFORE reading any result

A single value is a **draw from a distribution**, not a fact. Establish the noise band first, or you'll chase measurement scatter as if it were biology.

- **σ ≈ value × CV_within**, where **CV_within = √(CV_analytical² + CV_intra-individual²)**
- **"Nothing changed" band (95%)** ≈ baseline ± 1.96σ — where a repeat lands if nothing really moved.
- **RCV (reference change value)** = √2 × 1.96 × CV_within — how far two results must diverge before the change is real. (Both draws carry error, hence the √2.)

Approximate population CV_intra (%) — **not** this person's own; use as a prior and flag it:

| Very low noise (trust one value) | Moderate | **High noise (never decide on one draw)** |
|---|---|---|
| HbA1c ~2 · MCV ~1–2 · albumin ~3 · calcium ~2 | HGB ~3 · glucose ~5 · fT3/fT4 ~5–8 · creatinine ~5 · ApoB ~7 · cholesterol ~6 | **insulin ~20 · HOMA-IR ~23 · TG ~20 · TSH ~20 · ferritin ~15 · vitamin D ~12 · CRP >30** |

**The consequence people miss:** if a decision threshold sits **inside** the noise band, one measurement cannot resolve it. Example: HOMA-IR 2.0 → 1.5 is a 25% drop, but RCV for HOMA-IR is ~60% — statistically indistinguishable. **Say so** rather than flipping a decision on it; anchor on the low-noise marker (HbA1c) or repeat under identical conditions.

Corollary: prefer markers whose expected treatment effect **exceeds** their noise. If the intervention is expected to move a marker by less than its RCV, that marker can't verify the intervention.

## Step 4 — Confounders: the results that lie

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
6. Where relevant, the noise caveat: which results won't be trustworthy on a single draw.

**Interpreting results:**
1. Lead with **what changes** — the 1–3 numbers that alter a decision.
2. For each: value, direction vs last time, **whether the change exceeds RCV** (real) or not (noise).
3. Confounder check *before* conclusions.
4. Free computed ratios.
5. Then the normal/unremarkable, briefly.
6. Actions + the trigger for the next test, with a date.

## Boundaries

Reference ranges are **population** ranges, and "optimal" targets are a separate, often stricter claim — label which you're using. Interpretation is for a specific person with a specific history: **surface the decision and its reasoning, don't issue a diagnosis or prescribe.** Anything that changes a prescription goes through their doctor. Red-flag results (severe anemia, glucose in diabetic range, markedly abnormal liver/kidney function, calcium disturbance) → say plainly that this needs prompt medical review, and don't bury it.
