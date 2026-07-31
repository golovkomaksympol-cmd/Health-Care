---
name: plan-workout
description: Generate a strength-training plan for a specific day. Use when the user asks for a workout / gym session ("составь тренировку", "план на сегодня", "что делать в зале", "дай силовую"). Establishes the training goal first, then renders ONE day's session from the weekly skeleton + recent logs + today's readiness, picking from the exercise catalog filtered by gym. Outputs a single loggable session — not a generic plan.
---

# Plan-workout skill

Render **one day's strength session**: goal first, then the weekly skeleton, balanced against recent history, filtered by gym, adapted to today's readiness. **Pick from the catalog — never invent exercises or improvise off "last time" randomly.**

**Framework root** = the directory holding `Exercise Catalog.md` and `Models/` — `_core/` in a health-repo setup, or this bundle's root (`../../` from this file) standalone.

## Step 0 — Goal gate (ALWAYS FIRST, never skip)

Model: `Models/Effort-Frequency Trade-off (Look, Feel, Perform).md`. **A session is not designable until the primary driver is named**, because the driver — not the exercise list — sets effort-proximity, frequency and fatigue budget. Getting this wrong is the failure this gate exists to prevent.

**Establish the driver in this order:**
1. **Read it** from `<Person>/Practices` (weekly plan / goals section) or `<Person>/Health profile`. If a current block goal is documented, use it and **say which one you're using in one line**.
2. **Infer it** from the last ~5 sessions in `<Person>/daily/` if the pattern is unambiguous (e.g. consistently heavy compounds at low reps → PERFORM). State the inference and that you inferred it.
3. **Ask** if neither is available. One short question, offered as a choice — do not guess silently:

> "What's this block for — **LOOK** (size), **PERFORM** (strength / force transfer / sport), or **FEEL** (control, spinal health, low-load daily)?"

**The driver then binds the whole session:**

| Driver | Effort proximity | Session shape | Fatigue budget |
|---|---|---|---|
| **LOOK** | work close to failure on the target | more isolation volume, more sets per muscle | high — needs recovery days |
| **PERFORM** | high **intent**, *not* to failure | Power + heavy compounds lead; anti-movement core | high — recovery-capped |
| **FEEL** | **deliberately submaximal** | controlled, low-load, quality reps; can repeat daily | near-zero *by design* |

**Two hard rules from the model:**
- **Never program FEEL work near failure.** It converts it into LOOK work and destroys the frequency that makes it work.
- **One driver leads; others get a maintenance dose, not a competing one.** FEEL costs almost no fatigue and can run alongside either of the others.

If the request itself conflicts with the stated driver (e.g. "give me a brutal ab session" under a FEEL block), **say so and offer both options** rather than quietly serving the request.

### Dose-mismatch watch-list

These are the recurring errors the model exists to catch. **Check the assembled session against this list, and surface in the output only the one or two that actually apply today** — don't recite the list.

| Error | What it looks like | Correction |
|---|---|---|
| **Novelty instead of intent** | reaching for new exercises rather than contracting/bracing harder in known ones; repertoire growth feels like progress | keep the movement, raise the intent |
| **Frequency serving the wrong goal** | adding sessions to chase size; frequency is a motor-learning lever, not a substitute for proximity-to-failure or volume | if driver is LOOK, add effort/volume — not days |
| **Grinding control work** | FEEL work taken near failure | keep it submaximal so the frequency survives |
| **LOOK dose at FEEL frequency** | near-failure work attempted daily | accumulating fatigue, no result → cut frequency or cut effort |
| **FEEL dose at LOOK frequency** | low-load control work once a week | adapts nothing → raise frequency, keep it light |
| **Max effort on a bad day** | chasing a PR when readiness is down | quality over PR; deload is a legitimate FEEL-dose day |
| **Stacking novel eccentrics** | two new eccentric/plyo stimuli in one session | one novel stimulus at a time |

## Step 1 — Inputs (ask only what's still missing)
- **Gym / equipment available** → equipment filter. Use the person's gym list if there is one; otherwise ask which gym or what kit they have.
- **Time** (45 / 60 / 90 min) → volume / number of exercises.
- **Readiness**: sleep/HRV, soreness, injuries, illness, energy. If clearly fine → proceed; if low → deload (Step 4).
- Rotation day (A/B/C) and focus are **auto-selected** from recent logs unless the user names one.

## Step 2 — Read first (sources)
1. `<Person>/Practices` → the weekly plan section — session order, A/B/C rotation, rules, priorities.
2. `Exercise Catalog.md` (framework root) — the pick-list; respect tags/flags.
3. `<Person>/gyms.md` — filter to the chosen gym; if a needed item is `✗`/`?` → swap for same **pattern + adaptation**.
4. Recent `<Person>/daily/` (**last ~5 sessions**) — (a) balance/recovery: don't hammer the same pattern/muscle two days running; pick the rotation day that's **due**; (b) **last weights per exercise** for progression.
5. `<Person>/Health profile` — current injuries/illness + constraints.

### If there is no person folder (standalone / first-time use)
Sources 1, 3, 4, 5 won't exist. **Don't fail and don't invent history** — ask for the minimum in one short block, together with the Step 0 goal question:
- training days/week + which split (or offer a default A/B/C full-body rotation from `Training Framework.md`),
- equipment available,
- any injuries / medical constraints / movements to avoid,
- last session's main lifts + loads (for progression), or "first session" if none.

Then generate from `Exercise Catalog.md` + `Training Framework.md` alone, and state plainly that loads are **starting estimates** to be logged and corrected next time.

## Step 3 — Assemble (driver-weighted)
1. **Pick rotation day (A/B/C)** = least-recently done / restores weekly coverage. Avoid heavy same-muscle/pattern back-to-back vs the last session.
2. **Order:** warm-up + activation → **Power** (1 explosive, 3–5×1–5, fresh, max intent, **not to failure**) → **Strength** (≤3 heavy compounds, RIR 1–2; consecutive heavies must NOT share muscle/grip) → **Hypertrophy / patches** (under-covered patterns + weak links) → **Core / carry** (+ any rehab protocol due).
   - **Weight the blocks by the Step 0 driver:** PERFORM → Power/Strength get the volume, hypertrophy trimmed. LOOK → trim Power, expand hypertrophy sets and isolation, push proximity to failure on the target. FEEL → drop Power and heavy compounds entirely; the session *is* controlled low-load work and may be short and repeatable.
3. **Equipment filter:** include an exercise only if its `Equip` is available at the chosen gym; otherwise swap (same pattern/adaptation).
4. **Loading ladder for any new or rehab pattern:** enter at the step whose quality the person can own — isometric → anti-movement+fatigue → anti-movement+load → movement+fatigue → movement+load. Don't jump to loaded movement to look impressive.
5. **Coverage & patches:** check the week — fill under-trained patterns + **the person's own weak links as recorded in their `Health profile` / `Practices`** (typical classes: a rehab-flagged tendon, a lagging single-joint muscle, a side-to-side asymmetry, timing/activation faults). Don't assume weak links that aren't documented.
6. **Load:** pull the **last weight** from logs; **+ a small step if last set's RIR was easy**, hold/reduce if it was a grind. State the number.
7. **Time → volume:** 45 min ≈ Power + 2 strength + 1–2 patches + short core; 60–90 → add back-off sets / accessories / carries.
8. **Cue intent over novelty:** prefer a known exercise executed with more deliberate contraction/bracing over a novel one. Don't rotate exercises for variety's sake.

## Step 4 — Readiness adaptation
- **Low HRV / post-illness / poor sleep / notable soreness → DELOAD:** drop Power + heavy work; keep light full-range work + core/mobility, or skip. (Post-febrile: no intense work until HRV recovers.) Note that a deload day is a natural FEEL-dose day.
- **Flagged injury** → don't load it; swap (e.g. calf flare → no jumps / no toe-loaded carries).

## Step 5 — Constraints (always honor)
- **Read the person's documented constraints and honor every one** — they override any default here, and any driver. Map each to a rule, e.g.: *joint hypermobility / instability* → neutral spine, stability before load, `spine⚠` items controlled rather than ground out; *tendinopathy* → no fast eccentrics or plyo on that tendon, keep the loading protocol; *hypertension / cardiac flag* → no breath-holding or maximal straining.
- **Don't stack a NEW eccentric/novel stimulus** on top of another (CK spike / injury risk).
- **Power first, never to failure.** Strength quality over chasing PRs on bad days.
- If a constraint and the plan conflict, the constraint wins — say which exercise you swapped and why.

## Step 6 — Output (loggable — matches skill `log`)
Group by block (**Warm-up / Power / Strength / Hypertrophy / Core**). Per exercise: `Name — sets × reps, load, @RIR, rest` **+ the exercise's 🎥 link from the Exercise Catalog** so the trainee can review form. Copy the link from the catalog row; don't invent a URL.
- **First line: the driver** — `Driver: PERFORM (from Practices)` / `(inferred from last 5 sessions)` / `(you told me)`. Then a one-line rationale: which rotation day, what it balances, any readiness adjustment.
- **Last line: ⚠️ one watch-out**, picked from the Step 0 watch-list because it applies to *this* session — e.g. «эти же упражнения, но жёстче интент — не гоняйся за новыми» or «FEEL-блок: не до отказа, иначе теряешь частоту». One line, concrete, tied to what's actually in the plan. Skip it only if nothing on the list is genuinely at risk today.
- Power slot: prefer a pattern **not** trained recently (broaden the ProPower vector), and one that's practical in the trainee's gym (e.g. no med-ball throws without a wall → use cable rotation / plyo / jumps).
- End: «после — залогируй (skill `log`); добей 40 г белка в 1–2 ч».
Keep the plan tight; expand reasoning only if asked.
