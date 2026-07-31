# Cancer — Screening & Treatment

Half of a two-model pair (cause side: `Cancer - Etiology & Prevention.md`). The **detection → action** lens, collapsing the field to one action-question: *is this a **rabbit**, a **bird**, or a **turtle**?*

## Mechanism

### The screening "barnyard" (rabbits / birds / turtles)
Metaphor from the overdiagnosis literature (Welch). It is really a statement about **sojourn time** — the length of the detectable preclinical window:

- **Rabbits** — a *long* detectable preclinical phase → periodic screening **catches them in the pen.** Screening works; **chase these first.** Colorectal (adenoma→carcinoma, slow), most skin cancers (visible), cervical (HPV→dysplasia, slow).
- **Birds** — sojourn *shorter than any feasible screening interval* → already "flown" (metastasized) before detection. Screening the average-risk person mostly doesn't help. Pancreatic adenocarcinoma is the archetype. **Exception:** a known **germline predisposition / strong family history** turns a bird into a *surveillable* target (high-risk MRI/EUS protocols) — see the etiology model.
- **Turtles** — *never progress* to harm (indolent). Detecting them is **overdiagnosis**: chasing causes harm (surgery, radiation, anxiety) with **no benefit.** Some prostate (low-grade), papillary thyroid microcarcinoma, some DCIS, many incidental nodules. **Action = restraint** — this is where NNT/NNH says *don't screen / don't treat* (`NNT (Number Needed to Treat).md`).

**The uncomfortable core:** at the moment of detection you often **can't tell a rabbit from a turtle** — that ambiguity *is* the overdiagnosis problem, and why more screening is not automatically better.

### Treatment intensity follows the same triage
What a confirmed cancer turns out to be sets how hard to treat:
- **Rabbit** → curative local / definitive treatment (resection, etc.) — the payoff case.
- **Turtle** → **active surveillance over aggressive treatment** (low-grade prostate is canonical) — treating an indolent cancer is net harm.
- **Bird** → usually systemic / palliative; local heroics rarely change the trajectory.
- **Germline pharmacogenomics gate chemo dosing** — inherited metabolizer variants (e.g. DPYD for fluoropyrimidines, UGT1A1 for irinotecan, XRCC1 for platinum) change drug toxicity and must reach the oncologist *before* a regimen is chosen. (An individual's status is patient data — it lives in the Health Profile, not here.)

## Scale of simplicity

"What should I detect / how hard should I treat?" is intractable per-tumor. This model coarse-grains to **one 3-way question keyed to sojourn time — rabbit, bird, or turtle?** It collapses to: **chase rabbits on schedule, spare turtles, don't over-invest against birds (unless heredity makes them surveillable).**

**Usefulness test:** the moment you demand *bedside certainty* about which animal a fresh finding is, the model stops simplifying — that ambiguity is real and is the point. Use it to set **policy** (what to screen, how aggressively to treat a grade), not to label a single tumor with false confidence.

## Cynefin domain

- **Mechanism (screening detects a long-sojourn cancer):** **Complicated** — ordered, derivable from sojourn time.
- **Outcome (is *this* lesion a rabbit or a turtle; does treating it help *this* person):** **Complex** — you cannot classify with certainty at detection; benefit is emergent. Instrument (surveillance, grade, growth rate), don't assume.

## Time horizon (Lyapunov)

**Screening interval = the sojourn time.** Rabbits have a multi-year detectable window → periodic checks suffice; birds' window is shorter than any interval → screening can't win; turtles' is effectively infinite → never worth chasing. **Set the interval to the biology; don't invent one the sojourn time doesn't support.**

## Practice

- **Chase rabbits on schedule:** colonoscopy at guideline / personal-risk interval; skin checks; cervical (where applicable).
- **Birds:** don't over-screen the average-risk person; **do** convert to surveillance when germline / family history warrants (etiology model).
- **Turtles / restraint:** run any high-overdiagnosis screen through **NNT / NNH** before doing it (PSA = shared decision; **whole-body MRI marketing → incidentalomas / turtles**). More testing ≠ better.
- **Treatment:** match intensity to the animal (active surveillance for turtles, curative intent for rabbits); surface germline pharmacogenomics before chemo.

## Confidence

- **High:** the sojourn-time framing; rabbits (colorectal / skin / cervical) as screen-responsive; turtle / overdiagnosis reality; active surveillance for low-grade indolent disease.
- **Medium:** exact interval cut-offs (guideline-dependent, evolving); which emerging screens (MCED, LDCT) actually move birds toward rabbits.

## Falsification

**Attack — "rabbit / bird / turtle cleanly triages screening."** Counter: you **can't classify a screen-detected cancer at diagnosis** — that's the overdiagnosis problem; and some birds are becoming partially catchable (LDCT lung screening in smokers moved some toward rabbits; multi-cancer early-detection tests are trying). → **Qualified:** it's a *decision heuristic about sojourn time and screening policy*, **not a bedside classification.** Its real payload — *screening only helps rabbits, and chasing turtles causes harm* — survives; the clean 3-way labeling of an individual finding does not.

## Boundaries

- **Not diagnosis or oncologic management** — at an actual diagnosis this model steps aside for oncology; it sets screening policy and treatment *intensity philosophy*, not protocols.
- **Population / heuristic level** — cannot classify an individual tumor with certainty.
- **Ignores** staging systems, immunotherapy, the tumor microenvironment, molecular subtyping — all real, all below this scale.
- **Emerging screens** (MCED, LDCT, liquid biopsy) are shifting some boundaries — the rabbit / bird line is not static.
