# Iron Homeostasis

## Mechanism

Iron has **three independent absorption channels** in the gut, **one master regulator** (hepcidin), and **no excretion route** beyond cell shedding / menstruation. That asymmetry — easy in, hard out — is why both deficiency and overload are common, and why supplementation needs to be precise.

### Absorption

- **HCP1** (heme carrier protein 1): heme iron from animal protein. Fast, high-bioavailability (~15-35%). **Not blocked by coffee/tea/calcium/phytates** — the porphyrin ring protects the iron until it's inside the enterocyte.
- **DMT1** (divalent metal transporter 1): non-heme iron (Fe²⁺). Bioavailability ~5-15%, highly modulated by inhibitors. Blocked by **coffee chlorogenic acid** (-60% co-ingested), **calcium**, **phytates**, **polyphenols (tea)**. Enhanced by **vitamin C** (reduces Fe³⁺ → Fe²⁺).
- **LfR** (lactoferrin receptor): lactoferrin-bound iron, separate from both above. Useful adjunct — bypasses DMT1 blockers, modulates hepcidin downward (see below).

### Hepcidin = the master switch

- Hepcidin is the hepatic hormone that **binds ferroportin** (the only iron-export channel on enterocytes and macrophages) and **degrades it**. High hepcidin → ferroportin removed → absorbed iron stays trapped in the enterocyte → sloughed off into stool 1-2 days later.
- Hepcidin is **raised by**: inflammation (IL-6 → STAT3), high iron status, alcohol acutely, some infections.
- Hepcidin is **lowered by**: hypoxia, erythropoietic demand, low iron status, lactoferrin (modest).
- **Key clinical consequence:** a single iron dose spikes hepcidin for ~24-48 h, blocking the next dose. Hence **alternate-day non-heme dosing** (Stoffel et al. 2017, Lancet Haematology) has higher cumulative absorption than daily.

### Storage and signal

- **Ferritin** = the storage protein. Serum ferritin loosely reflects body stores, but it's also an **acute-phase reactant** — inflammation raises it independently of iron. A ferritin of 200 with hsCRP of 5 could mean overload OR inflammation.
- **Transferrin saturation** (TSAT, %) = serum iron / TIBC. Better than ferritin alone for distinguishing deficiency vs. inflammation: low TSAT with normal/high ferritin = inflammation; low TSAT with low ferritin = deficiency.
- **Hemochromatosis (HFE C282Y/H63D)** = genetic loss of hepcidin regulation → ferroportin always open → cumulative overload. TSAT typically > 45-50% before ferritin rises.

## Scale of simplicity

The complex system is whole-body iron: a distributed, hepcidin-governed loop of three absorption channels, ferroportin export, macrophage recycling, and hepatic storage — with the defining asymmetry that there is **no regulated excretion route**, so the system is one-directional and accumulating. Modelling all of that at once is intractable at the bedside. This model makes it simple by coarse-graining the entire loop to a **small readable panel dominated by ferritin (+ transferrin saturation)** as the proxy for body iron stores. The whole "how much iron does this body hold, and which way is it drifting" question collapses to a single readable number — **ferritin, with TSAT as the tie-breaker** — plus the accumulation prior that says: absent bleeding, iron only goes up.

At this scale the system becomes a workable object: one number to track over months, one dosing heuristic (feed a low channel, don't feed a full one), no need to reason about enterocyte kinetics or hepcidin transients in real time. That is the level of coarse-graining where iron homeostasis stops being a physiology problem and becomes a single-dial monitoring problem.

**Usefulness test:** the model earns its place only by collapsing the system to that readable ferritin/TSAT dial. Drop below this scale — into per-dose hepcidin transients, intracellular trafficking, erythropoiesis kinetics — and the system stays complex, non-predictive, and unmanageable in clinic; the model stops paying off. If at the ferritin-panel scale the picture is *still* ambiguous (it doesn't resolve to "feed / don't feed / investigate"), that is below-scale for this model — don't go there; hand off to the differential in `_core/Trigger Diagnostics.md`.

## Cynefin domain

- **Mechanism — Complicated.** Hepcidin → ferroportin degradation → trapped/exported iron is an ordered, expert-knowable causal chain. Given inputs (dose, timing, inflammation) you can predict the *acute* absorptive response.
- **Outcome — Complex.** Whether ferritin actually reaches target over months is emergent: occult GI loss, menstruation, microbiome, diet variance, adherence, and inflammation interact. Do not lend the Complicated mechanism's confidence to the whole-body trajectory — it is only knowable in hindsight, via measurement.

## Time horizon (Lyapunov)

- **Hours (24–48 h):** hepcidin refractory window — highly predictable; this is the mechanistic basis for alternate-day dosing.
- **Weeks (4–6):** early ferritin signal is a reasonable forecast in a non-inflammatory patient.
- **Beyond ~8–12 weeks:** trajectory prediction decays — if ferritin isn't moving, the model has exhausted its forecasting power. **Switch from predicting to instrumenting:** full panel (ferritin, TSAT, Hgb, hsCRP) and run the `_core/Trigger Diagnostics.md` differential rather than assuming the dose will "eventually work."

## Practice

### When iron is the limit (ferritin < 30 µg/L, or < 50 with symptoms / fT3 impairment)

- **Heme form first if tolerated** (bovine heme iron, e.g. Three Arrows Iron Repair). 20-40 mg heme/day, with breakfast. No timing dance around coffee — heme uses HCP1.
- **Non-heme as a second channel** (ferrous bisglycinate / sucrosomial): 25-30 mg elemental, **alternate days** with food (less GI burden than empty-stomach), **vitamin C 250-500 mg** co-administered for DMT1 reduction.
- **Coffee timing rule:** coffee at least 60 min **before** the non-heme dose; "coffee after" doesn't fully recover absorption (-39% at +60 min).
- **Lactoferrin** 100-200 mg/day with iron: third channel + hepcidin-lowering + selectively suppresses gram-negative gut pathogens. Cheap and additive.
- **Recheck cadence:** ferritin at 4-6 weeks for early signal; full panel (ferritin, TSAT, hemoglobin) at 8-12 weeks.

### When iron is the contraindication (ferritin > 100, or Hgb > 16, or TSAT > 45%)

- **Never supplement.** Add to STOP-list.
- If iron-deficient symptoms persist despite normal ferritin, look upstream (B12, folate, thyroid, occult bleed) — not at iron.
- If ferritin > 200 in non-inflammatory state (hsCRP normal): check HFE C282Y/H63D, TSAT trend; consider hemochromatosis workup.

### If iron supplementation isn't moving ferritin after 8-10 weeks

The differential is in `_core/Trigger Diagnostics.md` (occult GI loss, IBD, celiac, H. pylori, menorrhagia). Once those are ruled out: switch form (sucrosomial / IV).

## Confidence

- **High** on the three channels and hepcidin master role.
- **High** on alt-day non-heme superiority (Stoffel RCT).
- **Medium** on lactoferrin magnitude (modest individual effect; mechanism solid).
- **Medium** on optimal ferritin target — Medicine 3.0 wants 60-100; old labs accept 15-300.

## Falsification

**Target of attack:** the model's central *actionable* claim — that hepcidin's 24–48 h refractory window makes **alternate-day non-heme dosing superior**, i.e. that the feedback loop meaningfully governs real-world repletion.

**Strongest counter-evidence sought:** Stoffel et al. isotope RCTs (Lancet Haematol 2017; Haematologica 2020). The 2020 trial directly stress-tested the claim: in iron-depleted women, giving the *same total dose* as alternate-day vs consecutive-day single morning doses did **not** produce a significant difference in cumulative iron absorbed over the full course, even though fractional absorption *per dose* was higher on the alternate-day schedule. Several ferritin-endpoint trials also show daily dosing still raises ferritin adequately.

**Result — model survives, qualified.** The hepcidin-feedback mechanism is confirmed (fractional absorption per dose is genuinely higher when you skip a day), so the causal chain stands. But the *practical* payoff was overstated: over months, cumulative repletion is similar, so the real win of alternate-day dosing is **tolerability (fewer GI side effects) and efficiency per pill, not faster ferritin recovery**. Corrected inference: don't promise a patient faster repletion from alt-day — promise fewer side effects at equal result. The "one dose blocks the next" framing is directionally true but not a hard gate.

## Boundaries and doubts

- **Ferritin as inflammation proxy** muddies the signal. Always pair with hsCRP and TSAT when interpreting.
- **"Anabolic resistance" of iron in older patients** (anemia of inflammation, hepcidin-elevated states) — oral supplementation may fail entirely; IV is the realistic route.
- **Brand reliability of heme iron supplements** is uneven. Three Arrows had complaints in r/Anemic; Proferrin / Colorado Biolabs is the better-validated. Don't trust brand-X labels blindly — verify with a 4-6 week ferritin recheck.
- **Long-term hepcidin suppression** (chronic lactoferrin) — no obvious harm in current data, but not RCT-validated to years.
- **Scale/context edges:** scope is gut absorption (enterocyte HCP1/DMT1/LfR + ferroportin export) and systemic distribution (hepcidin, transferrin, storage) — it does *not* cover intracellular iron trafficking, erythropoiesis kinetics, or the iron–ferroptosis axis. The mechanism is cleanest at the enterocyte and noisier at the whole-organism readout. It holds in the **non-inflammatory** state, where serum ferritin ≈ body stores and the dosing logic applies. It **breaks as a stores-marker under inflammation/infection**: ferritin is an IL-6-driven acute-phase reactant, so inflammation falsely elevates it and a ferritin of 200 can coexist with true depletion — read TSAT + hsCRP instead of ferritin in that regime. Fasted vs fed and heme vs non-heme change *which* channel and inhibitor rules apply (coffee/calcium/phytate matter for DMT1 only).