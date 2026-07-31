# Training Adaptations — the 9 (Andy Galpin)

## Mechanism

Fitness is **not a scalar** ("fit / strong / trained") but a **vector of ~9 largely separable physiological adaptations**. Each has its own stimulus, its own test, its own protocol — and **transfer between them is limited or even negative** (SAID: Specific Adaptation to Imposed Demands). A lifelong marathoner can be near-untrainably weak in power; a bodybuilder can have poor VO₂max — and more of their own training will not move the other axis.

The 9 axes:
1. **Skill / technique** — nervous system executing a movement correctly, coordinated, efficiently. *(Deep-dive: `_core/Models/Skill & Technique (Galpin 1).md` — includes the mobility → stability → skill readiness foundation.)*
2. **Speed** — contract / move maximally fast with little load.
3. **Power** — max force in minimum time (speed × strength); explosive.
4. **Strength** — max force / 1RM against maximal resistance.
5. **Hypertrophy** — increase in muscle-fiber size/volume. *(Deep-dive: `_core/Models/Skeletal Muscle Hypertrophy.md` — this is axis #5 in detail.)*
6. **Muscular endurance** — repeated contractions / sustained tension resisting local fatigue.
7. **Anaerobic capacity** — near-max intensity 30–120 s, demand > O₂ supply.
8. **Maximal aerobic capacity (VO₂max)** — upper limit of O₂ uptake/use at max effort.
9. **Long-duration steady state** — moderate intensity 20 min+, cardio-respiratory + muscular.

## Scale of simplicity

The complex system is "whole-body fitness" — dozens of interacting physiological subsystems. The model makes it simple by coarse-graining to **~9 measurable performance phenotypes** (1RM, VO₂max, jump height, time-to-fatigue). At that scale the hard question ("am I getting fitter?") collapses to a tractable one: *which of the 9 axes do I want, and is each one's own test-number moving?* The move that buys the simplicity is refusing to reason below the phenotype — you don't model mitochondria or motor units, you apply a stimulus and read its axis-specific test.

**Usefulness test:** drop *below* this scale (predict the fitness vector from molecular pathways) and the system stays complex — the model stops paying off. Stay at the phenotype/test level. (Where even the phenotype scale degrades — see Boundaries.)

## Cynefin domain

- **Mechanism (does stimulus X drive adaptation Y?):** **Complicated.** SAID is ordered and predictable — apply the right stimulus, get the matching adaptation, test it directly. An expert can prescribe strength vs VO₂max work with high reliability.
- **Outcome (what does *this* person's whole-body fitness become over a training block?):** **Complex.** The 9 axes share substrates, compete for recovery, and interact with sleep/stress/age/genetics; the realized vector emerges and is only fully legible in hindsight. Never lend the Complicated confidence of "this stimulus → this adaptation" to the Complex question of "this program → this athlete's outcome."

## Time horizon (Lyapunov)

- **Weeks→months:** a specific stimulus reliably moves its own axis — this is the predictable window; program and forecast here.
- **Beyond ~a training block (months+):** interference, recovery debt, life stress, and individual response variance compound → the multi-axis outcome decays to noise. **Switch from predicting to instrumenting:** re-test each wanted axis on its own metric (1RM, bar speed, VO₂max, time-to-fatigue) on a fixed cadence and steer off the measurements, don't forecast the vector.

## Practice

- **Per-axis goal decision (the core use):** for each of the 9, decide explicitly — *do I want it? if no, why not? if yes, why?* This is goals → constraints applied to fitness. The program must then cover every **wanted** axis with its specific stimulus + test.
- **The goal set comes from the Centenarian Decathlon** (the physical tasks I want at 100 → which adaptations they require). Decathlon defines *what*; Galpin's 9 define *how* to train each.
- **Coarser goal layer:** when the question is *selection and dose for one body region* rather than *which of the 9 axes*, use `[[_core/Models/Effort-Frequency Trade-off (Look, Feel, Perform)]]`. Note it carves the space differently — its "Feel" (spinal health / motor control) is **not** one of the 9 adaptations, so the two models complement rather than nest.
- **Test each axis separately — don't infer one from another** (1RM for strength, vertical jump / bar speed for power, VO₂max test, time-to-fatigue for endurance, etc.).

## Confidence

- **High** that fitness is multi-dimensional and specificity dominates (SAID is bedrock exercise physiology).
- **Medium** on full independence between axes — see boundaries.

## Falsification

**The attempt:** the model's strong claim is that there are ~9 *largely separable* axes — i.e. that the number and independence are real, not an arbitrary taxonomy over shared machinery. Two serious attacks:

1. **Are the 9 truly independent, or one substrate wearing 9 masks?** If a single latent factor (general recovery / mitochondrial density / neural drive / total training tonnage) drove most of the variance, "9 axes" would be a bookkeeping convention, not a mechanism, and the practice ("train each separately") would be wasted effort. **Test:** factor-analytic and training-transfer evidence. Result — **survives, qualified.** Transfer studies repeatedly show specificity dominates (strength training barely moves VO₂max and vice versa; power and hypertrophy dissociate), so the axes are not one factor. But they are **not orthogonal either**: strength↔power and hypertrophy↔strength share real substrate, and endurance↔strength show *negative* coupling (interference). So the correct reading is **partially separable, non-orthogonal** — the model is directionally right, the "9 clean independent axes" framing is an idealization. Already reflected in Boundaries.

2. **Is SAID just a first-order approximation that fails at the edges?** The concurrent-training / interference literature is the strongest attack: high concurrent endurance *blunts* strength-hypertrophy (AMPK↔mTOR crosstalk), which pure "specific adaptation, limited transfer" doesn't predict — transfer can be **negative**, not merely zero. Result — **model qualified, not broken:** SAID holds as the first-order rule (right stimulus → right adaptation), but interference is a real second-order term that programming must handle by sequencing/separating competing axes. This *strengthens* the practical conclusion (test each axis; don't assume one covers another) rather than refuting it.

**Verdict: survives as a qualified model.** The taxonomy is an idealization (axes overlap and interfere), but the load-bearing claim — specificity dominates, transfer is limited-to-negative, so each wanted axis needs its own stimulus and its own test — is what the counter-evidence actually reinforces.

## Boundaries & caveats

- Axes are **not fully orthogonal**: shared substrates exist (strength underpins power; some hypertrophy supports strength; an aerobic base speeds recovery between anaerobic bouts).
- **Interference effect:** high-volume concurrent endurance can blunt strength/hypertrophy gains (and, to a lesser degree, vice versa). So "no mutual influence" is too strong — it is *limited transfer + sometimes negative interference*. Programming must sequence or separate competing axes.
- **With age, power and VO₂max decline fastest** and are the most often neglected — disproportionately important for healthspan / fall-prevention. Don't let "strength + hypertrophy" crowd them out.
- **Where the phenotype scale degrades:** assumes healthy, training-responsive humans with adequate protein/sleep/recovery, and holds best **novice→intermediate**. In the untrainable-sick, the heavily detrained, or at the elite tail, axes compete hardest for finite recovery and a global recovery bottleneck can swamp the "each axis needs its own stimulus" logic.
