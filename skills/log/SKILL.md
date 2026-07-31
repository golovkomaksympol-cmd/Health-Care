---
name: log
description: Record an activity into the person's daily journal (training, run, meditation, food, sauna, blood pressure). Use when the user says "log this" / "залогируй", or simply reports having done an activity. Tier 0 — short confirmation that shows exactly what was written; no analysis unless asked.
---

# Logging skill (Tier 0)

Record what the user did into the person's daily journal. Keep the reply **short**: confirm and show what was written. **No analysis** unless the user explicitly asks (then → skill `deep-think`). If the project defines intent routing (e.g. a root `CLAUDE.md`), follow it.

**Language:** reply in the **user's language**, whatever they wrote in. Write journal entries in the language the person's existing `daily/` files use — match the file, not this document. Keep exercise names and technical terms in English (see Format rules). This file is written in English; that is not the output language.

## Output contract
- Show the recorded lines so the user sees exactly what went in.
- If you augment an existing day's log, show the **merged** result together.
- Stay terse (bot format) — this is reflex, not reasoning.

## `daily/` structure
Path: `<Person>/daily/YYYY/MonthName/YYYY-MM-DD.md` (e.g. `daily/2026/April/2026-04-04.md`). Month folders named in English, capitalized (February, March, April, …). If the person's folder or `daily/` tree doesn't exist yet, create it on first log — don't ask.

Each file = one day. Header `## DD.MM.YYYY - Day name` (or a descriptive title). Body = activity sections with emoji-prefixed headers; **only what was actually done** appears. Append under the right header; create the file if missing.

Activity headers: **open the most recent `daily/` file first and reuse its headers verbatim** — same wording, same language, same emoji. Consistency matters more than any canonical list, because these files are read as a series. Only invent a header when that activity has never been logged before; then name it in the person's own language.

Typical activity classes and their conventional emoji (translate the label into the person's language):
| Emoji | Activity | What to capture |
|---|---|---|
| 🧘 | meditation | duration, quality, observations, insights |
| 🏋️ | strength training | exercises, sets, weights |
| 🏃 | interval / Zone 5 cardio | protocol, intervals, HR if known |
| 🚶 | walk / Zone 2 | duration, distance |
| 🎾 | sport / game | duration, intensity |
| 💃 | dance / class | type, duration |
| 🧱 | core routine | which drills, reps |
| 🧖 | sauna / cold | temperature, duration, rounds |
| 🍽️ | food | see Format rules |

### Relation to Practices
`Practices` = playbook (what each practice is, why, how). `daily/` = game tape (when it was done, what happened). If the user reports doing an activity → log it here. If the user changes a protocol or discovers something new about a practice → update `Practices` (that's a reasoning/edit task, not a Tier 0 log).

## Format rules
- **Strength**: no tables, line by line, canonical English exercise name. e.g. `Romanian Deadlift — 3 × 12, 70 kg`.
- **Food**: food header; lists not tables; per-meal macros computed **ingredient-by-ingredient** (never lump-sum), Casey Means / Good Energy lens; inline flags for seed-oil / fructose / polyphenols / ultra-processed; daily summary at the bottom. Look up recurring products in the person's `food_refs.md` first (if present) and reuse its flag vocabulary.
- **Time**: get current time via `python3 -c "from datetime import datetime; print(datetime.now().strftime('%H:%M'))"` — never ask.
- **Blood pressure / pulse**: log ONLY into the person's `lab.json` as longitudinal metrics (systolic / diastolic / resting pulse — **reuse the exact metric names already in that file**), not the daily file. Brief ack only.
- **Meditation**: store the user's words **verbatim** in the daily file (personal diary — no summarizing, no rephrasing, keep their original language). In the **reply**, do NOT echo the verbatim text — just acknowledge briefly ("recorded your observations", in their language). If the person's profile defines a reflection persona (e.g. a meditation-teacher synthesis), produce that reflection — it is the **one expansive exception** to Tier 0.

Person-specific details (food_refs, default ingredients, reflection persona, BP cadence) live in that person's own config/profile file if they have one — otherwise use the defaults above.
