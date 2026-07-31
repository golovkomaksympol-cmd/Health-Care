# Scientific Method (Measure Zero)

A **thinking protocol** for finding what's true in a complex, chaotic situation — not the textbook definition, an executable cycle. It is the epistemic engine underneath this library's whole **Falsification / Cynefin / Time-horizon** discipline (`AGENT.md`). Core stance: in a complex world the set of exactly-true answers has **measure zero**, so presume your hypothesis is wrong and **spend effort killing hypotheses, not confirming them.** Executable companion: the **empirical cycle (Mode A)** inside the `deep-think` skill.

## Mechanism

**The world it's built for:** complex/chaotic systems — nonlinear causation, small changes → big differences; "the brain is a prediction machine that loves pretty stories" and must be disciplined. The method is a **spiral, not a straight shot** — "an approximate method of approaching truth."

**The cycle (the lecturer's steps):**

- **0 · Task (the missing zeroth step).** Start from a task — it sets the **external criterion of truth** (Tarski: the truth-criterion must sit *outside* the system or it collapses). No task → "if you don't care where you go, any road takes you there." Make it **measurable** (number + range + horizon) — even a subjective scale ("count it in parrots") — because *if you don't measure, you don't care.* The task also fixes the **scale / precision / horizon** you can work at.
- **1 · Hypothesis.** "A hypothesis is what you're **ready to test** — not what you're willing to believe or do." Form: **if [cause] → [measurable result].** **Start thinking with a hypothesis, not by collecting data.** Formulate it so it **can be killed** — set the kill-criterion *in advance*. Make 2–5, pick the most probable, and **record why you picked it** (feeds the next cycle).
- **2 · Deduction (→ one-step prediction).** Pull a **concrete, checkable prediction** from the general hypothesis: "if it's true, doing X at time T, I'll see effect Y (a number)." **A precise prediction is possible for exactly one step** — the lightning: you can't say where it lands, but you *can* predict the next branch.
- **3 · Observation / experiment.** Plan what to measure; **change one factor per cycle**; record everything, especially the inconvenient; enough repetitions.
  - **3.1 Falsify first.** Ask: **"what must happen for me to honestly say this doesn't work?"** Then try to kill it. This is *falsifiability, not confirmation* — "you can confirm almost any nonsense; complex systems throw up illusory patterns." Failed prediction → cross it out, take the next hypothesis (Edison: "999 ways not to make a bulb"). A cheap, fast kill-test lets you **test against all the experts at once.**
  - **3.2 Verify (only after several failed kills).** This is **corroboration, not proof** — run a series, extend the horizon → "the best way we have *for today*."
- **4 · Generalize.** Turn the survivor into a **rule**; then ask **"beyond the result — what did we learn?"** → a **refined model.** Loop into a new cycle.

**Observation has two roles at two points of the loop — the loop has no true "start", it's a spiral:**
- **As a *test*, within a cycle:** hypothesis →(deduction)→ prediction → **observation**, compared against the prediction. Observation comes *from* the hypothesis — the **deductive arc**.
- **As a *source*, across cycles (loop-back):** the observation's results — especially **anomalies** ("странные результаты" → super-hypotheses) — breed the *next* cycle's hypotheses. This is "observation → hypothesis" — the **inductive arc**. Both arcs live in one loop.
- "Start with a hypothesis" is a **pedagogical corrective** against drowning in data, not a denial of induction: you may enter the loop from an observation ("I keep waking tired"), but the instant you do, convert it into a *testable hypothesis* rather than collecting more data.

**When do you "move to" falsification?** It isn't a later stage — it's *how you read the observation.* The moment an observation is in hand, compare it to the **pre-registered kill-criterion** — **modus tollens: if H→P and you observe ¬P, then ¬H.** You bias toward it *upstream*, at the deduction step, by designing the observation as a **kill-attempt (a severe test)**, and by trying to kill **first**. Verification is allowed only **after** the hypothesis survives several honest kill-attempts. So: *falsify the moment you have an observation; verify only after N failed kills.*

**The pointe: speed of iteration.** Slow cycles waste the method — the chaotic environment shifts faster than you learn. Kill **cheap and fast**; pivot before resources run out.

**Identity move:** "we don't become *right* — we **reduce the measure of illusion** and step closer." Replace "I was wrong" with "we got more precise; next cycle."

## Measure zero — what it means

- **Literal (chaos math):** in the phase space of a chaotic system the exactly-solvable stable trajectories occupy **measure zero** — "a mesh so fine you practically can't land on it." Consequence: **a trend is not a law of nature**; a straight line forever is a measure-zero event; **long-range linear prediction in a complex world barely exists** — every linear forecast needs a note saying *in what range it lives.*
- **Epistemic (the point):** "measure zero is the philosophical meaning that **most hypotheses we will kill.**" Because exact hits are vanishingly rare, **any given hypothesis is almost surely false** → the rational strategy is mass **elimination**, not accumulation of confirmations. Exact/rigid solutions *do* exist — but we mostly **build** them artificially (formal systems, programming languages); point them at the real world and "hello."

## Scale of simplicity

"How do I find what's true here?" is intractable in the abstract. This model coarse-grains it to a **repeatable protocol**: task → falsifiable hypothesis → one-step prediction → **try to kill** → verify survivors → rule. The simplifying move is **dropping the search for confirmation of a good story** and running **cheap kill-tests fast.**

**Usefulness test:** the protocol pays off where you can **cheaply and quickly test one factor.** Where no cheap discriminating test exists — untestable claims, or only slow / expensive / one-shot outcomes — the protocol stops simplifying (below-scale) → fall back to priors / statistics / base rates.

## Cynefin domain

- The method **is the Complex-domain instrument** — probe → sense → respond = hypothesis → observe → eliminate.
- **One cycle's mechanism is Complicated** (an ordered, derivable protocol). **The multi-cycle convergence on truth is Complex** — emergent, a spiral, legible only in hindsight. Don't lend one clean cycle's confidence to "therefore I've found the truth."

## Time horizon (Lyapunov)

The lecture's spine, and this library's: **a precise prediction is valid for one step / one cycle only** (the lightning branch). Beyond the cycle horizon, in a chaotic system, prediction decays to "a science-fiction novel" → **instrument (measure the next cycle), don't forecast.** Long-range linear prediction ≈ measure zero.

## Practice

1. **State the task measurably** — number + range + horizon; it's your external truth-criterion.
2. **Write 2–5 hypotheses** as *if cause → measurable result*; pick the likeliest, record why.
3. **Derive a one-step prediction** (X at T → Y).
4. **Pre-register the kill-criterion** — "what result makes me say it's false?" — change **one factor**, log everything.
5. **Try to falsify first;** killed → next hypothesis; strange side-results → save as candidate super-hypotheses.
6. **Verify survivors** with a series / longer horizon → "best for today."
7. **Generalize to a rule + capture what you learned;** start the next cycle.
- **Fast & cheap beats thorough & slow.** Separate the **practical test** (empirical, one case) from **statistics** (use stats only to *generate / rank* hypotheses, not to settle the instance).

## Confidence

- **High:** presume-wrong + pre-registered kill-criterion + one-factor + iterate-fast is a powerful practical thinking discipline; the falsify-before-confirm ordering; the one-step prediction horizon.
- **Medium:** the measure-zero **math→mind** transfer (a motivating metaphor, not a theorem — see Falsification); the "kill on first failure" rule (naive — see Falsification).

## Falsification

**Attack 1 — clean falsification is naive (Duhem–Quine / Kuhn / Lakatos).** You never test a hypothesis alone — only the hypothesis *plus* auxiliary assumptions; a failed prediction can always be pinned on an auxiliary, so a "clean kill" is an idealization, and real science does *not* abandon a theory on the first anomaly (research programmes persist through anomalies). → **Qualified:** you kill the hypothesis-**bundle**, not a lone claim; the lecturer's own discipline (pre-register the kill-criterion, change one factor, don't add conditions or blame reality) *mitigates* Duhem–Quine but can't erase it. "Kill on first failure" is a personal-decision heuristic, not how science actually converges.

**Attack 2 — "measure zero" is a metaphor smuggled from dynamics into epistemics.** The literal result is about stable orbits in a chaotic phase space; there is no measure on "the space of hypotheses," so "most hypotheses have measure zero" is analogy, not proof. → **Qualified:** keep measure zero as a *motivating stance* (presume your guess is wrong; exact answers are rare), not a mathematical claim about belief.

**Attack 3 — the cheap-fast bias systematically misses slow / rare / irreversible truths.** "Test in practice, not in statistics" and "kill fast" privilege problems that *have* a cheap discriminating test; for long-horizon, low-base-rate, or one-shot-irreversible questions the single practical test is underpowered (n=1), and the method discards truths it simply couldn't kill quickly. → **Real limitation:** there, priors / base rates / Bayes (and `NNT (Number Needed to Treat).md`) must carry the load; the method is for the **frontier**, not for rare-event estimation.

**Result — survives as a decision discipline for frontier problems, three qualifications:** clean falsification is Duhem–Quine-bounded (kill the bundle, discipline the auxiliaries), measure-zero is metaphor not theorem, and cheap-fast underserves slow / rare / irreversible questions (bring priors there).

## Boundaries

- **Precise prediction: one step only.** Past the cycle horizon → instrument, don't forecast.
- **Verification ≠ proof** — corroborated ≠ true; the configuration will shift. *Post hoc ≠ propter hoc.*
- **Checking is empirical (one case), not statistical** — statistics generates/ranks hypotheses, it doesn't settle the instance. (Inverse limit: for rare/slow outcomes you *do* need statistics — Attack 3.)
- **One factor per cycle**, or you can't read the result.
- **The real ceiling is psychological, not logical** — cognitive dissonance and "falling in love with the hypothesis"; most can't run even ~10 honest iterations without shifting the frame or blaming reality ("переобуваться"). The hardest instruction is *tolerate the gap between expectation and reality.*
- **For the frontier** — new, complex, under-specified situations "where even the specialist isn't a specialist." Inside rigid formal systems the chaos apparatus is unneeded (and where a formal system meets the real world — Gödel says hello).

## Source

Reconstructed from the lecture **«Логика в хаосе: Научный метод и мера ноль»** (course *Логика как фундамент мышления*). Executable companion: the empirical cycle (Mode A) inside the `deep-think` skill.
