# Browning — Maillard / Glycation

Deep-dive on **glycation = pathology #1** in `_core/Models/8-pathologies.md` ("substrate" class → food lever, not exercise; marker HbA1c).

## Mechanism

Non-enzymatic reaction: a **reducing sugar** (carbonyl) + an **amino group** (protein / lipid / DNA) → **Schiff base** → **Amadori product** (early glycation) → **advanced glycation end-products (AGEs)**, including cross-links. Same chemistry as food **"browning"** (searing / toasting / roasting = Maillard) — but in the body it runs slowly at 37 °C between blood sugars and tissue proteins. **HbA1c = glycated hemoglobin** (a glycation marker).

- **Always running** — spontaneous, non-enzymatic, unavoidable background process. Rate ↑ with sugar concentration, exposure time, temperature, and sugar type.
- **Reversible early, irreversible late:** Schiff base ⇌ and Amadori ⇌ are (slowly) reversible; but **AGEs / cross-links (e.g. glucosepane) are essentially irreversible** — the body can't readily remove them. The danger is precisely that the end-products don't undo.
- **Aging = formation vs clearance balance:** defenses (**glyoxalase** detox of methylglyoxal, AGE clearance, **protein turnover**) vs formation. If formation outpaces clearance → AGEs accumulate → tissue stiffening/dysfunction → faster aging. **Long-lived proteins (collagen, elastin, lens crystallin, myelin) are most vulnerable** — they turn over slowly/never, so no "reset" → AGEs pile up (stiff arteries/skin, cataracts).
- **Fructose glycates ~7–10× faster than glucose** (more open-chain reactive form + reactive carbonyl byproducts). Caveat: blood fructose is normally kept low (hepatic fructolysis), so *systemic* fructose glycation is limited — but high intake (HFCS, sugary drinks) and **intracellular fructose via the polyol pathway** (in hyperglycemia: glucose→sorbitol→fructose in lens/nerve/kidney) drive it. Per molecule, fructose is far worse.

## Scale of simplicity

Glycation's effect on the whole body is complex; the model makes it simple by coarse-graining to **one number — the glycemic regime, read as HbA1c** — acting on **long-lived proteins**. At that scale "am I glycating too fast?" collapses to "keep blood glucose low/stable (and fructose low)," with HbA1c as the single tripwire. The simplifying move is ignoring fast-turnover tissue (it resets before AGEs build) and not trying to model a lifespan number — you watch one marker.

**Usefulness test:** the model pays off where the glycemic regime is actually elevated (hyperglycemia / IR / diabetes). In a metabolically healthy, normoglycemic person endogenous formation is already near the floor — little left to simplify, marginal lever small (see Boundaries). Below the marker (predicting a hard lifespan endpoint from AGE chemistry) the system stays complex — don't go there.

## Cynefin domain

- **Mechanism → Complicated.** Ordered, predictable chemistry: given sugar concentration, exposure time, temperature and sugar type, formation rate follows. Expert-knowable, derivable from the causal chain.
- **Outcome (aging / hard endpoints) → Complex.** AGE accumulation is one node in a web (formation vs glyoxalase detox vs clearance vs turnover vs inflammation vs RAGE signaling); its net contribution to arterial stiffness, cataract, mortality is emergent and only legible in hindsight. Do not lend the chemistry's confidence to "less browning → longer life."

## Time horizon (Lyapunov)

- **HbA1c reflects the prior ~2–3 months** (RBC lifespan) — reliable predictive window for the glycemic-load signal.
- Long-lived-protein AGE burden integrates over **years–decades**; the *direction* (chronic hyperglycemia → more cross-links) is stable over that window, but the *magnitude* of the effect on any hard outcome is not forecastable — **instrument, don't predict:** track HbA1c (and, if warranted, skin-autofluorescence AGE reader) as tripwires rather than modeling a lifespan delta.

## Practice

- **Reduce formation (biggest lever):** keep blood glucose low/stable; **limit added fructose** (HFCS, sugary drinks, fruit juice) — the worse glycator.
- **Limit dietary (exogenous) AGEs:** high-heat dry cooking (fry / grill / sear / roast) generates AGEs; gentler/wetter methods (steam, boil, stew, lower temp, acidic marinades) produce far fewer. Browned/crispy = AGE-rich.
- **Support clearance:** exercise, avoid hyperglycemia, adequate protein turnover.
- Track via **HbA1c**.

## Confidence

- **High:** the chemistry (Schiff→Amadori→AGEs), late-product irreversibility, glucose control as the dominant endogenous lever, fructose's higher reactivity.
- **Medium:** the exact "7×" (range ~7–10×, context-dependent); how much *dietary* AGEs vs endogenously-formed AGEs drive human aging; whether cooking-method changes move hard outcomes.

## Falsification

**Attempt:** the model's action-relevant claim is that *dietary* AGE reduction (cooking method) meaningfully lowers AGE burden and risk. Strongest counter: if gut absorbs only a small fraction of ingested AGEs and endogenous formation dominates, then cooking method is near-irrelevant and the dietary-AGE lever is a mirage. Also tested against the aminoguanidine story — a compound that pharmacologically blocks AGE formation (mechanism sound) yet **failed to deliver clean clinical benefit** (ACTION trials halted / toxicity, no robust outcome win) — a direct "block the mechanism, get no outcome" challenge to the whole causal story.

**Result — qualified, core survives:** the *chemistry and endogenous-glucose lever survive intact* (HbA1c is a hard, reproducible glycation readout; hyperglycemia → cross-links is not in doubt). The *dietary-AGE branch is downgraded* — human absorption is fractional and endogenous formation plausibly dominates, so cooking method is a weak lever, not a primary one. The aminoguanidine failure did **not** falsify the mechanism (drug-specific toxicity + AGEs being one node among many, i.e. the Complex outcome), but it correctly caps confidence that intervening on AGEs alone moves hard endpoints. Net: mechanism kept, dietary/pharmacological-intervention claims held at Medium.

## Boundaries

- Covers glycation only — one of several aging pathways (#1 of 8; see `8-pathologies.md`).
- **"Reversible" applies ONLY to early steps** — do not generalize to AGEs/cross-links.
- **Dietary-AGE relevance is debated** — gut absorbs only a fraction of ingested AGEs; endogenous formation may dominate. Don't over-weight cooking method.
- For a **metabolically healthy** person (low glucose, no IR), endogenous glycation is already low → marginal value of extreme AGE-avoidance is small (diminishing returns).
- Anti-AGE / anti-glycation supplements (carnosine, aminoguanidine, etc.) — weak/uncertain human evidence.
- **Scale/context edges:** valid from single-reaction chemistry up to organ mechanics on **slow-turnover proteins** (collagen/elastin, lens crystallin, myelin, HbA1c); matters little in fast-turnover tissue (gut epithelium, blood cells). Does **not** by itself predict whole-organism lifespan. Dietary-AGE branch is context-valid mainly for high-heat dry-cooked diets.