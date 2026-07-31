---
name: deep-think
description: Single entry point / router for serious thinking. Use when the user asks to think something through properly ("think with me", "go deep", "break this problem down", "use the scientific method", "подумай со мной", "ответь глубоко", "разбери проблему"), asks "is it worth it / which is better / what would experts say", or faces a strategic, irreversible or protocol-defining question. Routes to an empirical cycle (cheaply testable) or an expert panel (judgment). Tier 2/3 — answers can and should be expansive, NOT the short bot format.
---

# Deep-think skill (Tier 2/3) — the single door

One entry point that **diagnoses where you are and routes you**: goal-gate → locate the problem → then either run the **empirical cycle** (Mode A, when there's a cheap falsification test) or convene the **expert panel** (Mode B, when it's judgment with no cheap test). The panel is a *generator* you can call inline from either mode. **Answers here can and should be long and developed** — overrides the default short bot format.

**Language:** reply in the **user's language**, whatever they wrote in. Keep technical and pharmacological terms in English (ApoB, mTOR, HOMA-IR, RIR) — translating them adds noise. This file is written in English; that is not the output language.

Shared spine for both modes: `Models/Scientific Method (Measure Zero).md` — **kill before confirm; presume your hypothesis is wrong.** The only difference between modes is *what kills the hypothesis*: **reality** (Mode A, empirical test) or an **adversarial red team** (Mode B, the best substitute when reality can't be cheaply queried).

## Step 0 — Goal gate (Munger's secretary; ALWAYS first)

Load goals/constraints from the person's profile (the goals file — `User Context` / `Human Context` / `Practices`, whichever name they use; if there's no profile, ask for the goal and the constraint in one line). Run the topic through three questions: **goal → constraint → necessary conditions.** This seat is led by the **Munger lens** (opportunity cost + inversion + the right to veto with "not worth attention"), with Goldratt beside it (*is this actually the constraint?*) and Gigerenzer (*is it even worth computing?*).

- If the topic is **not the current constraint, won't become one soon, and isn't a threatened necessary condition** → say so plainly: *not constraint-relevant → log it + a cheap tripwire, attention = zero* — and **STOP. Do not run the cycle or the panel.** (Escape hatch: cheap to do **and** an irreversible tail → still log + tripwire.)
- The secretary's main job is to **keep the discussion aligned to the goals and resist the "diligent helper"** — the urge to produce an impressive answer to a question that shouldn't have been asked.

## Step 0.5 — Locate & route (dispatcher)

Walk these four questions out loud and announce the route:

1. **Is there a task — and is it well posed?** A task supplies the **external criterion of truth** (Tarski — the criterion sits outside the system). Make it measurable: **number + range + horizon** (arbitrary units are fine, as long as it's countable; *if you don't measure, you don't care*). Reformulate vague asks ("I want to sleep better", "I want to know the truth") into something measurable first. If there's no real task → back to Step 0 (log + tripwire, stop).
2. **Which stage am I at?** Name the point in the cycle: no task / task but no hypotheses / hypotheses but untested / observations but unread / a rule already. Then work **from that point**, not from scratch.
3. **Can this simply be falsified?** Is there a **cheap, fast** empirical test that discriminates between the hypotheses?
   - **YES → Mode A (empirical cycle).** Go query reality; don't convene a panel to rationalise a pretty story.
   - **NO** (values / strategy / no cheap test) **→ Mode B (judgment panel).**
4. **Do I need hypotheses or different angles?** The panel is your **generator** — of hypotheses, observations, and ways to kill them. Call it **inside** either mode whenever your own material runs short.

---

## Mode A — Empirical cycle (the scientific method)

Model: `Models/Scientific Method (Measure Zero).md`. The cycle is a **spiral, not a single shot**; the priority is **speed and cheapness of each turn**.

1. **Task** — measurable criterion + horizon (from Step 0.5).
2. **Hypotheses** — 2–5, each stated as **`if [cause] → [measurable result]`**, and each with its **kill criterion** written down immediately (what would refute it). Start **from a hypothesis, not from data collection.** Pick the most probable one and **record why.** *(Short on ideas → convene the panel as a generator.)*
3. **Deduction → a one-step prediction:** "if this holds, then under X, within time T, I will see Y (a number)." Precise prediction extends **one step only**.
4. **Observation:** the **cheapest** test that works; change **one factor**; record everything, especially the inconvenient parts.
5. **Falsify FIRST.** Trigger: the moment an observation is in hand, check it against the kill criterion you wrote in advance (*modus tollens: H→P; you observe ¬P ⟹ ¬H*). Design the observation as an **attempted kill** (a severe test), not a confirmation. Killed → next hypothesis. Anomalies → set aside separately, as candidate super-hypotheses.
6. **Verify** only what has survived several kill attempts → that is **corroboration, not proof**; a series of them, or a longer horizon → "the best approach available today".
7. **Generalise** into a rule + **"what did I learn → refined model"** → next turn of the spiral.

- **Anti-patterns** (name them out loud if they creep in): shifting the frame after a failure, stacking extra conditions, blaming reality, confirmation-hunting (forcing the evidence to fit), a single anecdote taken as proof, and **falling in love with the hypothesis**. Statistics are for generating and ranking hypotheses; the individual case is settled by practice.

---

## Mode B — Judgment panel (for questions with no cheap test)

### B1 — Refine the question first
Do **not** rush to answer. The one who asks already senses the answer — draw it out and sharpen what's truly being asked.
- Restate the question back, sharper than posed. Strip vagueness; name the implicit goal (what is optimized, against what constraint).
- Surface hidden assumptions and what would actually change the user's decision.
- If the real question differs from the literal one, say so and offer the reframe.
- Briefly reflect what the user likely already believes — that belief is **data**, and the panel will test it, not flatter it.
Proceed only once the question is crisp. If genuinely ambiguous, ask one tight clarifying question first.

### B2 — Select experts (topic **and** meta-topic)
From `mentor-panel.md` (framework root). **Only those who genuinely have something to say** — on the **topic** (domain experts) **and** on the **meta-topic** (the kind of question: decision under uncertainty, systems/strategy, behavior change…). 2–4 total + one **additional** relevant world-expert on the subject **not** on the mentor panel.

### B3 — Run each expert in a separate thread (parallel)
Spawn **one sub-agent per expert** (Agent tool), all in a single message → **parallel / independent**. This structurally enforces "independent views before conflict" — experts cannot converge by agreeing in sequence. Each gets the refined question, its lens, and the relevant data files (`Health profile`, `lab.json`, `Practices`, recent `daily/`). Each reasons **only** from its lens, **hypotheses → validate → conclude** (no jumping), and returns its strongest independent take + where it thinks the user is wrong.

### B4 — Synthesize with anti-sycophancy
Full contract: `meta-thinking.md` (framework root). The three non-negotiables:
1. **Name the expected answer, then forbid it** — surface only what contradicts or extends it.
2. **Mandatory red team** — ≥1 expert on the opposite conclusion (premortem: "assume this failed in 2 years — why?"). No unanimous panels. *(This red team IS the falsification for a non-empirical question.)*
3. **Falsifiable tripwire per conclusion** — measurement + when it would prove the conclusion wrong. *(Same object as Mode A's kill-criterion.)*
Ground every claim in the person's data, not vibes.

## Models
Reusable models live in `Models/` at the framework root (`_core/Models/` in a health-repo setup; `../../Models/` relative to this file when installed standalone). Pull the relevant one in rather than reasoning from scratch.
