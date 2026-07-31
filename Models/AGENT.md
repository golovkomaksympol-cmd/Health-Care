# Models

Working mechanistic models of reality — the ones that actually change a practice. Not idealized textbook biology; **minimally correct models of sufficient accuracy** (Munger).

## Format (per model file)

Each file documents one mechanism with the same shape:

- **Mechanism** — the causal chain in just enough detail to derive a practice from it.
- **Scale of simplicity** — the level of coarse-graining at which this model **collapses a complex system into a simple, workable object** — one robust heuristic, one triangle picked out of the fractal. State that scale explicitly (molecule / organ / whole organism; which tissue/subsystem). Then apply the **usefulness test:** *if the system is still complex at the scale the model offers, the model is not worth applying here — drop it.* A model earns its place only by making something tractable. Simplicity is **local and borrowed**: "Earth is flat" is simple *and* accurate at room scale and breaks at radio-signal scale — pick the model whose simple scale matches your problem. (Where the model's simplicity *stops* holding — the regime/context edges — goes in Boundaries, not here.)
- **Cynefin domain** — Complicated (ordered, predictable via mechanism) / Complex (emergent, causality only in hindsight) / Chaotic. State it for **both** the mechanism and the outcome it's applied to — a mechanism can be *Complicated locally yet Complex globally*; never lend mechanistic confidence to a complex, whole-system outcome.
- **Time horizon (Lyapunov)** — over what window the model actually predicts (hours / days / months / years / decades). Beyond it, in a complex-chaotic system prediction decays to noise → **switch from predicting to instrumenting** (measure/tripwire, don't forecast).
- **Practice** — the actions that follow from the mechanism (specific, executable).
- **Confidence** — how strong the evidence is. "High on the core, medium on the timing details" beats false certainty.
- **Falsification** — **not optional.** Before recording a model, make a *genuine, serious* attempt to disprove it (strongest counter-evidence, the best case that it's wrong — MR/RCT/base-rates/a contradicting mechanism). **Record the attempt AND the result:** did the model survive, get qualified, or fail? A model with no falsification attempt is not ready to be written.
- **Boundaries and doubts** — where the model breaks down, what's unresolved, what's a black box. **Not optional** — a model without stated limits is dangerous.

## When to write a new model file

A new file in `Models/` is warranted when:

- A causal mechanism is **actively driving** a practice in one or more patient files (i.e., it would be referenced from there).
- The mechanism is **universal** — applies to any patient with the relevant biology, not just one person.
- The mechanism is **non-obvious** — the practice that follows from it isn't the default popular advice.

## When NOT to write a model file

- Pure textbook biology that doesn't change any specific recommendation.
- One-off observations about a single patient (those belong in the patient's `Medical Profile.md`).
- Speculation without enough evidence to derive a practice. Better to leave a stub `❓` in an existing model than to write a thin file.
