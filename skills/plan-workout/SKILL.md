---
name: plan-workout
description: Generate a strength-training plan for a specific day. Use when the user asks for a workout / gym session ("составь тренировку", "план на сегодня", "что делать в зале", "дай силовую"). Renders ONE day's session from the weekly skeleton + recent logs + today's readiness, picking from the exercise catalog filtered by gym. Outputs a single loggable session — not a generic plan.
---

# Plan-workout skill

Render **one day's strength session** from the weekly skeleton, balanced against recent history, filtered by gym, adapted to today's readiness. **Pick from the catalog — never invent exercises or improvise off "last time" randomly.**

## Step 1 — Inputs (ask only what's missing)
- **Gym / equipment available** → equipment filter. Use the person's gym list if there is one; otherwise ask which gym or what kit they have.
- **Time** (45 / 60 / 90 min) → volume / number of exercises.
- **Readiness**: sleep/HRV, soreness, injuries, illness, energy. If clearly fine → proceed; if low → deload (Step 4).
- Rotation day (A/B/C) and focus are **auto-selected** from recent logs unless the user names one.

## Step 2 — Read first (sources)

**Framework root** = the directory holding `Exercise Catalog.md` and `Models/` — i.e. `_core/` in a health-repo setup, or this bundle's root (`../../` from this file) when installed standalone.

1. `<Person>/Practices` → the weekly plan section — session order, A/B/C rotation, rules, priorities.
2. `Exercise Catalog.md` (framework root) — the pick-list; respect tags/flags.
3. `<Person>/gyms.md` — filter to the chosen gym; if a needed item is `✗`/`?` → swap for same **pattern + adaptation**.
4. Recent `<Person>/daily/` (**last ~5 sessions**) — (a) balance/recovery: don't hammer the same pattern/muscle two days running; pick the rotation day that's **due**; (b) **last weights per exercise** for progression.
5. `<Person>/Health profile` — current injuries/illness + constraints.

### If there is no person folder (standalone / first-time use)
Sources 1, 3, 4, 5 won't exist. **Don't fail and don't invent history** — ask for the minimum instead, in one short block:
- training days/week + which split (or offer a default A/B/C full-body rotation from `Training Framework.md`),
- equipment available,
- any injuries / medical constraints / movements to avoid,
- last session's main lifts + loads (for progression), or "first session" if none.

Then generate from `Exercise Catalog.md` + `Training Framework.md` alone, and state plainly that loads are **starting estimates** to be logged and corrected next time.

## Step 3 — Assemble (per §2.6)
1. **Pick rotation day (A/B/C)** = least-recently done / restores weekly coverage. Avoid heavy same-muscle/pattern back-to-back vs the last session.
2. **Order:** warm-up + glute activation → **Power** (1 explosive, 3–5×1–5, fresh, max intent, **not to failure**) → **Strength** (≤3 heavy compounds **3×5**, RIR 1–2; consecutive heavies must NOT share muscle/grip) → **Hypertrophy / patches** (8–15 reps on under-covered patterns + weak links) → **Core / carry** (+ Alfredson if due).
3. **Equipment filter:** include an exercise only if its `Equip` is available at the chosen gym; otherwise swap (same pattern/adaptation).
4. **Coverage & patches:** check the week — fill under-trained patterns + **the person's own weak links as recorded in their `Health profile` / `Practices`** (typical classes: a rehab-flagged tendon, a lagging single-joint muscle, a side-to-side asymmetry, timing/activation faults). Don't assume weak links that aren't documented.
5. **Load:** pull the **last weight** from logs; **+ a small step if last set's RIR was easy**, hold/reduce if it was a grind. State the number.
6. **Time → volume:** 45 min ≈ Power + 2 strength + 1–2 patches + short core; 60–90 → add back-off sets / accessories / carries.

## Step 4 — Readiness adaptation
- **Low HRV / post-illness / poor sleep / notable soreness → DELOAD:** drop Power + heavy 3×5; keep light full-range work + core/mobility, or skip. (Post-febrile: no intense work until HRV recovers.)
- **Flagged injury** → don't load it; swap (e.g. calf flare → no jumps / no toe-loaded carries).

## Step 5 — Constraints (always honor)
- **Read the person's documented constraints and honor every one** — they override any default here. Map each to a rule, e.g.: *joint hypermobility / instability* → neutral spine, stability before load, `spine⚠` items controlled rather than ground out; *tendinopathy* → no fast eccentrics or plyo on that tendon, keep the loading protocol; *hypertension / cardiac flag* → no breath-holding or maximal straining.
- **Don't stack a NEW eccentric/novel stimulus** on top of another (CK spike / injury risk).
- **Power first, never to failure.** Strength quality over chasing PRs on bad days.
- If a constraint and the plan conflict, the constraint wins — say which exercise you swapped and why.

## Step 6 — Output (loggable — matches skill `log`)
Group by block (**Warm-up / Power / Strength / Hypertrophy / Core**). Per exercise: `Name — sets × reps, load, @RIR, rest` **+ the exercise's 🎥 link from the Exercise Catalog** (the DeltaBolic channel-search URL) so the trainee can review form. Copy the link from the catalog row; don't invent a URL.
- One-line top rationale: which rotation day, what it balances, any readiness adjustment.
- Power slot: prefer a pattern **not** trained recently (broaden the ProPower vector), and one that's practical in the trainee's gym (e.g. no med-ball throws without a wall → use cable rotation / plyo / jumps).
- End: «после — залогируй (skill `log`); добей 40 г белка в 1–2 ч».
Keep the plan tight; expand reasoning only if asked.
