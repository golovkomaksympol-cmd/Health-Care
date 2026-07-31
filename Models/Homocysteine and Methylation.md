# Homocysteine and Methylation

## Mechanism

Homocysteine sits at the crossroads of **one-carbon metabolism**, the cellular pathway that supplies methyl groups for DNA, neurotransmitters, phospholipids, and creatine. Elevated homocysteine = the pathway is congested somewhere; the marker itself is the alarm, not the cause.

### The cycle (compressed)

```
Methionine
    ↓ (ATP)
SAM (S-adenosyl-methionine) — the universal methyl donor
    ↓ donates -CH3 to DNA / neurotransmitters / etc.
SAH (S-adenosyl-homocysteine)
    ↓
Homocysteine ── two routes ──┐
    │                        │
    │ remethylation          │ transsulfuration
    │ back to methionine     │ (one-way out)
    │                        ↓
    ↓                      CBS (B6)
   MTR (B12)  + 5-MTHF       ↓
   MTRR (reactivates B12)  cystathionine
                              ↓
   alternative: BHMT       cysteine → glutathione
                  + betaine
```

### Key enzymes and the gene variants that gate them

- **MTHFR** (C677T, A1298C) — converts 5,10-methylene-THF → **5-methyl-THF**, the form that donates methyl to homocysteine. C677T homozygous TT cuts activity ~70%; heterozygous CT ~35%. Means dietary folate / folic acid is not enough — must supplement with **5-methyl-THF (methylfolate)** to bypass the block.
- **MTR** (rs1805087) — methionine synthase; the enzyme that uses B12 + methyl-THF to remethylate homocysteine.
- **MTRR** (rs1801394) — reactivates the B12 cofactor inside MTR. When MTRR is impaired (GG variant), the B12 cofactor falls into the inactive (cob(II)alamin) state and can't be salvaged. Standard **cyanocobalamin** is not optimal — needs **methylcobalamin** (the active form that bypasses the MTRR reactivation step).
- **CBS** (less commonly tested) — alternative exit via transsulfuration, B6-dependent.
- **BHMT** — backup remethylation using betaine (TMG) as methyl donor; B12-independent. The reason TMG appears in "homocysteine regulator" stacks — gives a second path when B12/folate cycle is impaired.

## Scale of simplicity

The complex system is one-carbon metabolism — a densely coupled web of enzymes, cofactors, and methyl-transfer reactions feeding DNA, neurotransmitters, phospholipids, and glutathione. The model makes it simple by coarse-graining that entire web down to **one readable number: plasma homocysteine**. At that scale the question "is my methylation cycle / B-vitamin status OK?" collapses to "is Hcy in the 5-12 µmol/L band, and does it fall when I supplement?" — a single functional readout standing in for the whole pathway.

That simplicity is *local*: it holds for status-reading ("am I methylation-adequate?") and breaks the moment you stretch the same number into a causal lever ("lowering Hcy prevents CVD events") — the scale where B-vitamin RCTs falsified it. Hcy is a good status marker, not a proven causal handle. **Usefulness test:** the model earns its place only where the one-number collapse makes the system tractable; if at the scale you're working the system stays complex — you're chasing hard endpoints through Hcy, or the number won't move the decision — that's below-scale, drop it, don't go there.

## Cynefin domain

- **Mechanism (the pathway):** **Complicated** — ordered and predictable. Given a genotype and a form of vitamin, the direction of the biochemical effect (homocysteine falls) is reliable and mechanistically derivable.
- **Outcome (does lowering it help the patient):** **Complex** — emergent, whole-system, causality mostly visible only in hindsight. A congested methylation cycle sits upstream of dozens of processes; that homocysteine *moves* tells you little about whether the disease endpoint moves. Never lend the Complicated confidence of the biochemistry to the Complex clinical outcome.

## Time horizon (Lyapunov)

- **Biochemical response:** predictable over **6-8 weeks** — the recheck window. Plasma homocysteine reliably tracks the intervention within this window.
- **Clinical outcome (brain atrophy, cognition, vascular events):** predictability decays over **years**; beyond ~1-2 years the causal attribution to homocysteine specifically is noise. Past the biochemical window → **stop forecasting benefit, start instrumenting:** track homocysteine, B12/folate status, and the actual downstream endpoint (cognitive testing, imaging where indicated) rather than assuming the marker's movement equals protection.

## Practice

### Targets

- **Optimum (Medicine 3.0):** 5-7 µmol/L. No published RCT shows mortality benefit *below* ~10; below ~7 risks overshoot (folate excess has its own concerns — see Boundaries).
- **Acceptable / standard target:** < 12 µmol/L. The OPTIMA trial cutoff (B-vitamins reduced brain atrophy in patients with homocysteine > 13).
- **Action threshold:** > 12 µmol/L → start B-vitamin combination; recheck in 6-8 weeks.

### Lever stack (in order of yield, by typical genotype scenario)

| Scenario | Add this | Why |
|:---|:---|:---|
| **Standard, no genotype info** | Methylfolate 400-800 µg + methylcobalamin 500-1000 µg + P5P (B6) 25-50 mg | Covers MTR cycle from both ends; methylated forms work regardless of MTHFR / MTRR variants |
| **MTHFR C677T positive** | Same, but **must use methylfolate**, not folic acid | Folic acid in MTHFR-impaired patients accumulates as unmetabolized folic acid (UMFA), masks B12 deficiency on labs |
| **MTR / MTRR variants** | Same, but **must use methylcobalamin** (not cyanocobalamin) | Active B12, bypasses MTRR reactivation step |
| **Homocysteine > 12 despite full vitamin stack** | Add TMG (betaine) 1-3 g/day | Engages BHMT backup path; bypasses entire B12/folate cycle |
| **Homocysteine high + low glutathione signs** | Add NAC 600 mg/day | Pulls homocysteine down the transsulfuration arm toward glutathione |

### Form precision matters

- **Folate:** L-methylfolate (Quatrefolic, Metafolin) — active form. Avoid folic acid (synthetic, requires MTHFR conversion).
- **B12:** methylcobalamin (active) or adenosylcobalamin (mitochondrial form). Avoid cyanocobalamin in any patient with MTR/MTRR variants.
- **B6:** P5P (pyridoxal-5'-phosphate, active) preferred over pyridoxine HCl in high doses.

## Confidence

- **High** on the pathway topology, gene variants, and the methylation-bypass logic.
- **High** on the OPTIMA finding (B-vitamins reduce brain atrophy in elevated-homocysteine patients).
- **Medium** on the absolute target. "5-7" is optimum extrapolation; "< 12" is the threshold with solid outcome evidence.
- **Low** on whether driving homocysteine below ~10 yields net benefit. No RCT, and folate-related concerns push back (see Boundaries).

## Falsification

**Attempt.** The serious challenge to this model is the causal one: if elevated homocysteine is a *lever* for disease, then lowering it with B-vitamins should lower events. This was tested directly and at scale in cardiovascular outcomes:

- **HOPE-2** (2006, ~5500 pts): folic acid + B12 + B6 lowered homocysteine but did **not** reduce the primary composite of CV death / MI / stroke.
- **NORVIT** (2006, post-MI): B-vitamin lowering gave **no benefit**, with a signal of *harm* in the combined folate + B6 arm.
- **VITATOPS** (2010, post-stroke, ~8000 pts): homocysteine fell, but **no significant reduction** in recurrent stroke / MI / vascular death.

Mendelian-randomization and meta-analyses of these B-vitamin RCTs converge: for **cardiovascular** endpoints, homocysteine behaves as a **marker, not a causal lever** — it co-travels with risk (renal function, B-vitamin status, inflammation) rather than driving it.

**Result — qualified, split by outcome:**

- **CVD arm: FAILED.** The claim "lower homocysteine → fewer cardiac/stroke events" does not survive. Treat homocysteine as a marker here, not a target to chase for cardioprotection.
- **Neuro arm: SURVIVED (narrowly).** **OPTIMA / VITACOG** (Smith et al., 2010) showed B-vitamins slowed brain atrophy specifically in patients with baseline homocysteine > 13 and adequate omega-3 status. This is the cleaner, still-standing signal and is why the model is retained — but scoped to the CNS/cognitive-decline outcome, in the elevated-homocysteine subgroup, not as a general "lower is better."

Net: the *mechanism* is intact; the *outcome claim* is trimmed to the neuro/elevated-baseline case and stripped of its cardiovascular justification.

## Boundaries and doubts

- **Homocysteine is a marker, not the cause.** Lowering it does not always translate to outcome benefit — multiple RCTs of B-vitamin supplementation in CVD failed to reduce cardiac events even though homocysteine fell. The OPTIMA brain-atrophy result is the cleaner signal.
- **Folate excess and cancer risk:** unmetabolized folic acid (UMFA) may stimulate growth of pre-existing premalignant cells. Aim for the lowest effective dose, prefer methylfolate, don't stack supplemental folate on a fortified-grain diet without need.
- **Thyroid interaction:** hypothyroidism (low fT3) slows methionine cycle independently of vitamins; treating thyroid often drops homocysteine 1-2 µmol/L without changing supplements. Fix thyroid first, recheck.
- **Renal function:** chronic kidney disease impairs homocysteine clearance — high homocysteine with eGFR < 60 has different meaning than in healthy kidneys.
- **B12 deficiency masked by folate:** classic teaching — folate supplementation can normalize the macrocytic anemia of B12 deficiency while neurological damage progresses. Always assess B12 status before pushing folate alone.
- **Scale/context edges:** the model spans enzyme/cofactor kinetics at the cellular level up to whole-organism plasma homocysteine as the readout. It's applied primarily to the CNS outcome (brain atrophy / cognitive decline), secondarily to vascular endothelium — do not extend "lower is better" to hard cardiovascular endpoints (that's where it breaks, see Falsification). Valid in the ambulatory adult with adequate renal function and euthyroid state; degrades / shifts meaning in CKD (impaired clearance), hypothyroidism (cycle slowed independently of vitamins), and pre-existing B12 deficiency (folate masks it). Genotype-specific form precision (methylfolate / methylcobalamin) is where it earns its keep vs. generic B-vitamin advice.

