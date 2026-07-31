---
name: create-model
description: Write a new mechanistic model file, or audit/upgrade an existing one. Use when the user says "создай модель" / "запиши модель" / "add a model", proposes a mechanism worth capturing reusably ("this explains why X works"), or asks to review a model for rigor. Enforces the model format including a mandatory falsification attempt — and will refuse to write a model that doesn't earn its place.
---

# Create-model skill

Models are **working mechanistic models of reality — the ones that actually change a practice.** Not textbook biology; *minimally correct models of sufficient accuracy* (Munger). The authoritative format spec is `Models/AGENT.md` at the framework root (`_core/Models/` in a health-repo setup, `../../Models/` from this file standalone) — **read it first**; this skill operationalizes it.

Output goes to `Models/<Name>.md`.

## Step 1 — The gate (run BEFORE writing anything)

All three must be true. If any fails, say which and **stop** — propose the alternative instead of writing a file.

| Gate | Test | If it fails |
|---|---|---|
| **Drives a practice** | Does a concrete, executable action change because of this mechanism? | It's interesting biology, not a model. Don't write it. |
| **Universal** | Does it apply to anyone with the relevant biology, not just this person? | It's a personal finding → the person's `Medical Profile` / `Health profile`, not `Models/`. |
| **Non-obvious** | Does the practice differ from default popular advice? | Textbook content the reader already knows. Don't write it. |

Also **don't write** when there isn't enough evidence to derive a practice. A `❓` stub inside an existing model beats a thin new file.

**Check for an existing home first.** Search `Models/` — if a model covers this mechanism, **extend it** rather than forking a near-duplicate. Two files on one mechanism guarantee divergence. (If a near-duplicate already exists, say so and offer to merge.)

## Step 2 — Draft the sections

Every model has the same eight-part shape. Fill each deliberately; empty ceremony is worse than omission.

1. **Mechanism** — the causal chain, in *just enough* detail to derive a practice. Stop at the level where the next link stops changing what you'd do.

2. **Scale of simplicity** — the coarse-graining level where the complex system collapses into a **simple, workable object**. State it explicitly (molecule / tissue / organ / whole organism — which subsystem). Then apply the **usefulness test**: *if the system is still complex at the scale the model offers, the model is not worth applying here — drop it.* A model earns its place by making something tractable. Simplicity is **local and borrowed**: "Earth is flat" is simple *and accurate* at room scale, and breaks at radio-signal scale. Pick the scale that matches the problem. *(Where simplicity stops holding goes in Boundaries, not here.)*

3. **Cynefin domain** — Complicated (ordered, predictable via mechanism) / Complex (emergent, causality only in hindsight) / Chaotic. State it for **both** the mechanism **and** the outcome it's applied to. A mechanism is often *Complicated locally yet Complex globally* — **never lend mechanistic confidence to a complex whole-system outcome.**

4. **Time horizon (Lyapunov)** — over what window this actually predicts (hours / days / months / years / decades). Beyond it, prediction decays to noise → **switch from predicting to instrumenting** (measure, set a tripwire; stop forecasting).

5. **Practice** — the specific, executable actions that follow. If you can't write this crisply, the mechanism isn't understood well enough yet.

6. **Confidence** — asymmetric and honest. "High on the core, medium on the timing details" beats one flat number.

7. **Falsification — not optional.** Before recording the model, make a *genuine, serious* attempt to disprove it: strongest counter-evidence, the best case that it's wrong — Mendelian randomization, RCTs, base rates, a contradicting mechanism. **Record the attempt AND the result:** did it survive, get qualified, or fail? *A model with no falsification attempt is not ready to be written.* See Step 3.

8. **Boundaries and doubts** — where it breaks down, what's unresolved, what's a black box. **Not optional** — a model without stated limits is dangerous.

## Step 3 — The falsification pass (the part that gets skipped)

This is the step that separates a model from a rationalization. Spine: `Models/Scientific Method (Measure Zero).md` — **kill before confirm.**

Do this **actively**, not as a formality:
1. State the model's strongest **prediction** — what must be true if it holds.
2. Go looking for **evidence that it isn't.** Search for the contradicting trial, the null MR study, the population where the effect is absent, the competing mechanism that explains the same observation.
3. Ask the **confound question**: what else would produce this same pattern? (Reverse causation, confounding by a third factor, selection effects, regression to the mean.)
4. Record the verdict honestly: **survived** / **survived but narrowed to <scope>** / **failed**.

**A failed falsification is a successful use of this skill.** If the mechanism doesn't survive, say so and don't write the file — or write it with the boundary drawn tightly around where it *did* hold. Never quietly drop a disconfirming finding.

Anti-patterns to name if they appear (see `meta-thinking.md`): condition-stacking until it can't be wrong, confirmation-hunting, single anecdote as base rate, falling in love with the hypothesis, mechanistic overreach.

## Step 4 — Place and wire it

- **File:** `Models/<Descriptive Name>.md`. Match the existing naming style (title case; qualifier in parentheses where it disambiguates, e.g. `ProPower (Power & RFD)`).
- **Cross-link both directions.** Add `[[Models/<Name>]]` links from related models and from the practice/profile sections that rely on it. **A model nothing links to will be forgotten** — if you can't name an inbound link, re-check Gate 1.
- If the model supersedes an older file, say so explicitly and propose deleting the stale one (don't leave two).
- Keep it dense. These are read as LLM context: tables over prose, no padding, no textbook recap.

## Step 5 — Report back

Show: the file path, the gate verdict, **the falsification attempt and its result**, and the cross-links added. If any section is genuinely uncertain, leave a `❓` marker rather than smoothing it over — a visible gap is more useful than false completeness.

## Auditing an existing model

Same spec, applied backwards. Score each of the eight sections present/absent/thin, then report the highest-value repair. In practice the two most common failures are: **no real falsification attempt** (section is ceremonial), and **missing Boundaries** — which is the dangerous one, because a model without stated limits gets applied outside its regime. Also check that the Cynefin call doesn't lend mechanistic confidence to a complex outcome, and that the stated time horizon matches how the model is actually used.
