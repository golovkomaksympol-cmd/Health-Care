# Cost Latency

Deciding to push harder because *it feels fine right now* — when "right now" is before the bill is posted. The failure isn't weak discipline; it's **reading a sensor that measures the wrong quantity.** The felt state is an honest estimate of **present capacity** and a biased estimate of **future cost** — and the bias runs one way: toward *more*.

## Mechanism

**Cost latency** = the delay between an action and the moment its cost becomes perceptible. **Decision interval** = how often you get to decide. The whole model is the comparison of those two durations.

When `cost latency > decision interval`, three things stack:

1. **Different clocks.** The felt state tracks *fast* variables (arousal, substrate, CNS drive, mood, cash on hand). The cost accrues in *slow* ones (connective tissue, technical debt, receivables, trust, tolerance). They are not merely lagged — they are driven by different state variables, so they can move in opposite directions at the same instant.
2. **Zero is the null reading.** An unposted cost and a nonexistent cost produce the **identical sensor reading**. So the error isn't random noise around the truth; it is a floor at zero. Every reading understates or ties — never overstates. That makes the bias **directional**, which is why the fix cannot be "average more readings".
3. **The signal is actively muted at the decision point.** Adrenaline, endorphins, flow, deadline pressure, stimulants, leverage — the same conditions that make the moment feel good are the ones that suppress the damage signal. Worse, in many systems **the good feeling *is* the buffer being spent**: alertness at 1 a.m. is adenosine masked by stress hormones; feeling flush is spending float. There the naive read inverts — the pleasant signal is evidence *of* consumption, not of surplus.

**Why the asymmetry justifies a rule and not just caution.** Under lag you can't see which regime you're in, and the two errors are usually not symmetric in **reversibility**: an under-dose is recoverable at the next interval; an over-dose can remove several intervals (injury, blown budget, credit event, burnout). Benefits of the extra push tend to be small and linear; costs are occasionally large and nonlinear.

**The remedy is not restraint — it's a clock change.** Don't discard the observation and don't act on it now: **record it, and decide at the next planning point, after the latency has elapsed and the bill is visible.** This converts an unusable real-time signal into a usable delayed one. You lose only the impulse.

### The lever ladder

When you *do* push, levers differ on two independent axes — **how fast the cost shows** and **whether you'll be able to tell what caused it.** Climb from the top.

| Lever | Cost latency | Attributable? | Notes |
|---|---|---|---|
| **Raise intent / quality** on what's already planned | immediate | yes | free, reversible mid-action |
| **+1 unit** of something already in the plan | short | yes | cheap, targeted |
| **+load / +scope** on an existing element | medium | yes | belongs on the slow clock |
| **Add a new element** | long | **no** | worst on both axes |

A new element is worst not only because its cost is slow, but because it makes the delayed bill **unattributable** — change three things and the delayed signal is noise. This is `[[Models/Scientific Method (Measure Zero)]]`'s *one factor per cycle*, applied to costs instead of hypotheses.

**The free lane.** Levers with genuinely ~zero delayed cost (by construction, not by hope) can be added in the moment — that is where the impulse should go. Naming that lane in advance is what makes the rule survivable; a rule with no outlet gets overridden.

## Scale of simplicity

"How hard should I push?" is intractable in the abstract — it depends on the domain, the physiology, the person, the history. This model coarse-grains it to **one comparison of two durations**: *cost latency* vs *decision interval*. That single comparison decides which clock the decision belongs on. Everything else — magnitude, timing, individual tolerance — is deliberately left out.

**Usefulness test:** where the cost lands **inside** the decision interval (a hot stove, a compile error, a rep that stalls mid-set, a price that moves against you on the tick), the feedback is honest and immediate — the model adds nothing. **Drop it and just read the feedback.**

## Cynefin domain

- **Mechanism: Complicated.** Why lag produces a floored-at-zero sensor is derivable — different time constants, masked signalling, identical null reading.
- **Outcome: Complex.** Whether *this particular* extra push costs anything is emergent and legible only in hindsight. Never lend the mechanism's clarity to the instance: the model predicts the **sign of the bias**, not that today will hurt.

## Time horizon (Lyapunov)

The model predicts **one thing, one step**: the direction of the error at the moment of decision. It predicts neither the magnitude nor the arrival time of the cost for any instance. Past that → **instrument, don't forecast**: log the felt observation with the load, read it after the latency has elapsed, and let the paired record — not the memory of the feeling — set the next dose.

## Practice

1. **Name the cost latency before starting** — "how long until I would know this was too much?" A number, even rough.
2. **Compare it to the decision interval.** Latency ≤ interval → ignore this model, use the feedback. Latency > interval → the rest applies.
3. **Pre-commit the dose on the slow clock** — decided *before*, from the log, not *during*, from the feeling.
4. **Spend the good feeling as data, not as action:** record it against the load ("planned dose felt like 60% effort"), and cash it at the next planning point.
5. **Climb the lever ladder from the top** if you push at all; never enter at "new element" on an impulse.
6. **Change one thing per cycle**, or the delayed bill can't be attributed.
7. **Keep the free lane explicit** — pre-list the ~zero-cost additions the impulse is allowed to take.
8. **Audit the slow clock periodically.** If the planning point never raises the dose, the model is being used as cover for under-dosing — see Boundaries.

## Confidence

- **High:** the structural claim (lag ⇒ floored-at-zero, one-directional bias); the remedy (move the decision to a clock slower than the latency); one-factor-for-attribution.
- **Medium:** that the felt signal is *actively muted* at the decision point — well evidenced in acute exertion and stress physiology, more analogy in organizational and financial settings.
- **Low / context-dependent:** the exact ordering of the lever ladder outside training; the size of the reversibility asymmetry in any given domain (this must be argued per case, not assumed).

## Falsification

**Attack 1 — "this is hyperbolic discounting with new labels."** If it is, it adds nothing: known bias, known fixes (commitment devices, framing). → **Qualified, not killed.** Discounting is *preferential* — the agent knows the later cost and prefers the sooner reward anyway. Here the cost is **not perceived at all**, and the perception itself is biased by the mechanism above. The remedies differ accordingly: discounting is treated with precommitment against a known quantity; cost latency is treated by **instrumenting and re-clocking** an unknown one. Sibling, not synonym.

**Attack 2 (the strongest) — the rule cancels itself, because under-dosing also has an unposted bill.** Chronic conservatism produces no progression, atrophy, missed windows — and *that* cost is equally invisible inside the decision interval. Applied symmetrically the model gives no direction at all. → **Qualified, and it narrowed the model.** The model does not say "hold back"; it says "decide on the slower clock", and the slow clock is exactly where the dose is *raised* deliberately. The tie is broken only by **asymmetric reversibility**. **Where the two errors are symmetrically reversible, this model offers no guidance and must not be used** — that boundary came from this attack.

**Attack 3 — base rates / NNT.** How often does "felt good, added a bit" actually cost anything? Usually nothing. A rule that suppresses the impulse *every* time pays a certain small price to avoid a rare event — poor NNT. → **Real limitation.** The rule earns its place only where the tail is fat enough or the recovery long enough to dominate the arithmetic. Run `[[Models/NNT (Number Needed to Treat)]]` on it before adopting it in a new domain; in low-tail settings it is overhead, not discipline.

**Attack 4 — sometimes the feeling is valid information.** Readiness is a real physiological state; subjective readiness, HRV and movement speed do carry signal. Dismissing the feeling wholesale discards a working sensor. → **Correct, and it sharpened the model rather than breaking it.** The felt state is a **valid estimate of present capacity** and a **biased estimate of future cost** — two different quantities. Legitimate use: letting it modulate how the *already-planned* work goes. Illegitimate use: letting it authorise *unbudgeted new load*. The model now says which reading to trust for what, instead of "don't trust yourself".

**Result — survives, narrowed.** Holds where (a) cost latency exceeds the decision interval, (b) the two errors differ in reversibility, and (c) the tail is fat enough to pass NNT. Outside those three conditions it is overhead. Attacks 2 and 4 did most of the shaping: the model is not "resist the impulse", it is "**the sensor is right about capacity and biased about cost — so move the cost decision to a clock that can see it.**"

## Boundaries & doubts

- **Latency ≤ decision interval → don't use it.** Immediate honest feedback needs no protocol.
- **Symmetric reversibility → no guidance.** Both errors have hidden bills; the model can't break the tie.
- **Thin tail → NNT says it costs more than it saves.** Not every impulse deserves a governor.
- **Predicts sign, not magnitude.** It never says how big the unposted cost is, or whether this instance has one at all.
- **"The good feeling is the buffer being spent" is solid in acute physiology, analogy elsewhere.** Don't state it as mechanism in a social or financial system without arguing the specific buffer.
- **Its own failure mode is rationalized under-dosing.** The model is a perfect hiding place for risk aversion: every refusal to progress can be dressed as respect for latency. The instrument against this is that the slow-clock decision must *actually happen* and must sometimes raise the dose. **If the planning point never increases anything, the model is not being used — it is being hidden behind.**
- **Black box: the latency itself.** People estimate "how long until I'd know" badly, and it varies with age, training state, and history. Treat the estimate as a hypothesis to be corrected from the log, not as a known constant.

## Source

Applied companions: `[[Models/Effort-Frequency Trade-off (Look, Feel, Perform)]]` — where this shows up as *novelty instead of intent* and as dose/frequency mismatch; `[[Models/Scientific Method (Measure Zero)]]` — one factor per cycle, kill before confirm; `[[Models/NNT (Number Needed to Treat)]]` — whether the rule earns its place in a given domain; `[[Models/Signal-vs-Noise in Lab Practice]]` — any single reading is an estimate, not the value.
