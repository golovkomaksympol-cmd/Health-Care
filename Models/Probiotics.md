# Probiotics

The **intervention** — swallowing live microbes — and why it's usually the wrong tool against the gut ecosystem (the system itself: `_core/Models/Gut Microbiome.md`).

**Problem this model fixes:** the reflex co-prescription — *"you're on antibiotics → your flora will be wrecked → take probiotics."* That is the **doctor's model, and it's the flawed one.**

## Mechanism

- **Why the reflex is wrong** (three counts): (1) antibiotic disruption isn't universal and usually isn't symptomatic — AAD hits a minority of courses (see Gut Microbiome); (2) a **~dozen-strain commercial capsule cannot re-seed a several-hundred-species ecosystem** — scale mismatch, and the strains are mostly transient / non-engrafting; (3) blanket probiotics can even **delay** the native microbiome's return to baseline (Suez et al. 2018, *Cell* — introduced strains squat and crowd out the natives).
- **The one place a probiotic has real logic — during the course, only if there's diarrhea:** **_Saccharomyces boulardii_** — a **yeast**, therefore intrinsically **resistant to antibacterial antibiotics**, so it survives alongside the course. Best-evidenced probiotic for **preventing/attenuating AAD and C. diff recurrence.** It does **not** "restore flora" — it transiently holds the line while the antibiotic runs.
- **Restoration is not the probiotic's job** — that's the ecosystem's own, fed by fiber + fermented foods (`Gut Microbiome.md`). A capsule doesn't manufacture the ecosystem.

## NNT — applied here

The decision lens itself lives in `_core/Models/NNT (Number Needed to Treat).md` (how many to treat for one to benefit; lower = better; recompute for *your* baseline risk). Applied to probiotics:

- **AAD prevention:** NNT ≈ **10–13** (adults), ~9 (children) → of ~10 treated, **~9 get no benefit.** Real but modest.
- **C. diff prevention:** NNT ≈ **42 overall**, dropping to **~12 in high-baseline-risk** populations.
- **The load-bearing point — NNT falls as baseline risk rises**, which is exactly *why* this model says "targeted, not reflexive": low-risk person → high NNT (waste + possible harm); high-C.diff-risk course → NNT into the useful range.

## Scale of simplicity

Against a several-hundred-species ecosystem, a probiotic is a tool applied at the **wrong scale** — that's the whole failure of the doctor's model. This model makes the *intervention decision* simple by coarse-graining not to species but to **symptom × baseline risk:**
- no symptom, low risk → don't intervene (NNT too high);
- diarrhea, or high C. diff risk → one specific strain (*S. boulardii*), where NNT is low;
- restoration → feed the ecosystem, not a capsule.

**Usefulness test:** the moment the question becomes "which species do I install to fix the ecosystem," you're below-scale — the model tells you to stop and hand the problem back to the ecosystem (Gut Microbiome).

## Cynefin domain

- **Mechanism — Complicated:** a yeast is unaffected by antibacterials; a strain either survives transit or doesn't. Derivable.
- **Outcome — Complex:** whether a given probiotic colonizes / helps / harms *this* person is emergent ("permissive vs resistant" colonizers, Suez). Don't lend the mechanism's confidence to the individual outcome; steer by NNT + symptoms.

## Time horizon (Lyapunov)

The effect is **during-course / short-term**; commercial strains show **no durable engraftment** → don't expect a capsule to change the long-run microbiome. Judge it on the near-term symptom (AAD averted?), not on a lasting-flora promise.

## Practice

- **Default on an antibiotic course: no routine probiotic** (NNT too high, disruption usually silent and self-repairing).
- **If AAD develops during the course:** **_S. boulardii_** — the evidence-based pick. Use it *prophylactically* only in **higher-risk** situations (elderly, high C. diff risk, high-risk antibiotic) — i.e. where NNT is low.
- **After the course: don't "restore" with a capsule** — feed the native ecosystem (`Gut Microbiome.md`).
- **Red flags override:** fever, bloody / severe / persistent diarrhea → medical (possible C. diff), not a probiotic.

## Confidence

- **High:** capsule diversity ≪ ecosystem; *S. boulardii* has the best AAD/C.diff evidence; NNT for AAD is modest (~10); blanket use unsupported.
- **Medium:** that standard probiotics *delay* reconstitution (one strong but small, endoscopy-based study — Suez 2018).

## Falsification

**Attempt — the load-bearing claim is "routine probiotics with antibiotics are pointless, possibly harmful."** Strongest counter: **Cochrane and strain-specific RCTs show benefit** — *S. boulardii* and *L. rhamnosus* GG **reduce AAD and C. diff** (NNT ~10–13 for AAD). If that holds, "pointless" is false.

**Result — survives, sharpened (NOT "all probiotics are useless"):** the evidence splits by the *scale of the claim*.
- **Blanket, multi-strain, "just-in-case" for everyone:** *not* supported — **AGA (2020) recommends against** probiotics for most GI indications, with a **narrow conditional exception** for specific strains to *prevent C. diff* in patients on antibiotics (targeted, not reflexive); plus Suez's plausible harm to recovery. This half stands.
- **A specific strain for a specific job** (*S. boulardii*/LGG in an at-risk course): **does** have RCT support. So the corrected model is **"stop using probiotics as a reflex ecosystem-repair tool; use one specific strain for one specific symptom/risk (where NNT is low), and otherwise feed the native ecosystem."**
- The **NNT itself is the evidence made honest:** ~10 for AAD = real but "9 of 10 gain nothing" → only worth it as baseline risk rises. The **Suez "delays recovery"** caution is kept at **Medium** (single study).

## Boundaries

- **Prevention framing only — not C. diff *treatment*** (that's vancomycin / fidaxomicin, FMT).
- **Real harm in the vulnerable:** in the **critically ill, immunocompromised, or central-venous-catheter** patient, probiotics — *S. boulardii* included — can cause **fungemia / bacteremia.** Contraindicated there.
- **Individual colonization is unpredictable** — no capsule reliably engrafts.
- **Doesn't cover** infant/neonatal (NEC prophylaxis is its own literature), IBS/IBD strain-specific evidence.