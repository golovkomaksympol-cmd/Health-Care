# Mentor panel — how it works (shared framework)

A sanity-check / multi-angle reasoning device used by the `deep-think` skill. The **roster is per-person** — look for a "Mentors panel" section in the person's context/practices file (its exact filename varies: `User Context`, `Human Context`, or `Practices`). If the person has no roster, fall back to the domain list below. This file is the generic method.

## Method
1. Pick **only 2–4 mentors relevant to the domain** + evidence-based medicine (Cochrane) as the floor. Don't summon the whole roster.
2. Generate each view **independently** before surfacing conflict (don't let them converge by agreeing in sequence).
3. Enforce anti-sycophancy (`_core/meta-thinking.md`): forbid the expected answer, mandatory red team, falsifiable tripwire.
4. Ground every claim in the person's data (`lab.json` / `Practices` / `daily`).

## Domains

### Systems & strategy

- **Peter Senge** — systems thinking (*The Fifth Discipline*). Look for feedback loops, delays, leverage points.
- **Eliyahu M. Goldratt** — Theory of Constraints. What is the bottleneck right now? Optimizing anything else is waste.
- **Richard Rumelt** — strategic thinking. Diagnosis → guiding policy → coherent actions. Avoid "bad strategy" (goals-as-strategy).

### Thinking & decision-making

- **Shane Parrish / Farnam Street** — mental models, general thinking concepts.
- **Gerd Gigerenzer** — risk literacy, decision-making under uncertainty. Translate scary stats into natural frequencies before reacting.
- **Nassim Taleb** — antifragility, asymmetry of risk, fooled by randomness.
- **Dan Heath** — *Switch*, *Decisive*, *The Power of Moments*, *Upstream*. Behavior change, decision design, prevention.

### Evidence & medicine

- **Evidence-based medicine / Cochrane** — the baseline for what's actually known vs assumed.
- **Medicine 3.0 — Peter Attia** — proactive, personalized, longevity-oriented framing.

### Behavior & habits

- **James Clear** — habits as the substrate of long-term outcomes.
- **Thaler & Sunstein** — nudge, choice architecture, behavioral economics.

### Training & performance

- **Andy Galpin** — exercise physiologist; **strength / performance coach**. Frame every training question as: *which of the 9 adaptations are we targeting? is the stimulus specific to it? what's the test? are we creating interference?* Fitness is a vector, not a scalar. Model: `_core/Models/Training Adaptations (Galpin 9).md`.

## How to use the panel in a discussion

When weighing a new intervention or protocol change, explicitly ask:
- *Gigerenzer:* What's the absolute risk, not the relative risk? What's the number needed to treat?
- *Goldratt:* Is this attacking the actual bottleneck, or a comfortable adjacent target?
- *Taleb:* What's the tail risk? Is the cost of being wrong bounded?
- *Heath (Upstream):* Are we treating a downstream symptom when the upstream cause is fixable?
- *Cochrane / EBM:* Is there real evidence, or just mechanistic plausibility?