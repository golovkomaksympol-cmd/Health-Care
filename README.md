# Health OS

A reasoning engine for working on your own health with an LLM: **five Claude Code skills** plus the shared framework and mechanistic models they run on.

This is the generic half of a personal health repo — extracted so it can be used and improved by other people. **It contains no personal or medical data about anyone.** Your data stays in your own private repo.

> ⚠️ **Not medical advice.** This is a thinking and record-keeping tool, not a clinician. It is built to *surface decisions and their reasoning* — so you can have a better conversation with your doctor. Nothing here diagnoses or prescribes. Anything that changes a medication goes through a professional.

## The skills

| Skill | What it does |
|---|---|
| **`lab-panel`** | Design a blood panel, or interpret one that came back. Tiers every test by *"would this change an action?"*, models measurement noise (RCV) before calling a trend real, and names the confounders that fake results. |
| **`plan-workout`** | Render **one day's** strength session — from your weekly split, balanced against recent history, filtered by the equipment you actually have, adapted to today's readiness. Picks from a catalog rather than inventing exercises. |
| **`deep-think`** | A router for serious questions. Gates on whether the topic is even your current constraint, then runs either an **empirical cycle** (when a cheap falsification test exists) or an **adversarial expert panel** (when it's judgment). |
| **`log`** | Record what you actually did into a dated journal. Deliberately terse — capture, no lecture. |
| **`create-model`** | Write a new mechanistic model, with a gate that refuses models which don't earn their place and a **mandatory falsification attempt**. |

## Install

**As a plugin** (recommended — you get updates):

```bash
/plugin marketplace add werdan/health-os
```

Then install the `health-os` plugin and invoke skills as `/health-os:lab-panel`, `/health-os:plan-workout`, etc.

**Or just clone it** — copy the `skills/` directories into your project's `.claude/skills/`, and keep the rest of the repo alongside as the framework root.

`/plugin` isn't available in the web/mobile UI. To use these in a cloud session, declare the marketplace in your repo's committed `.claude/settings.json` so it loads at session start.

## How it fits together

```
health-os/
├── skills/          the five skills
├── Models/          mechanistic models — the "why" that drives a practice
├── *.md             frameworks: decision principles, sleep, training,
│                    nutrition, screening, trigger diagnostics, meta-thinking
└── Exercise Catalog.md
```

Skills read the framework files by relative path, so the same skill works whether this sits at `_core/` inside a bigger repo or stands alone as a plugin.

Pair it with a private repo holding one folder per person:

```
your-health/
├── _core/                    ← this repo (git subtree)
└── You/
    ├── Health profile.md     labs, diagnoses, constraints, overrides
    ├── Practices.md          your protocols and weekly plan
    ├── lab.json              longitudinal results
    └── daily/YYYY/Month/     the journal `log` writes to
```

Every skill degrades gracefully: with no person folder it asks for the minimum it needs instead of failing.

## Design principles

A few opinions are baked in, and they're the actual point:

- **A test must change an action.** If the result wouldn't alter the plan, it's anxiety, not information.
- **One measurement is a draw from a distribution, not a fact.** Establish the noise band before declaring a trend. If a decision threshold sits inside the noise, say so instead of flipping the decision.
- **Kill before confirm.** Models carry a *recorded* falsification attempt and its result. A model with no stated boundaries is dangerous.
- **No unanimous panels.** Multi-perspective reasoning runs views in parallel and requires a red team, so agreement can't be manufactured by going in sequence.
- **Universal here, personal there.** Anything true for one person only belongs in their file, never in the framework.
- **Simplicity is local.** Every model states the scale at which it collapses a complex system into something workable — and fails the usefulness test if it doesn't.

Framework conventions live in [`AGENT.md`](AGENT.md); the model format in [`Models/AGENT.md`](Models/AGENT.md).

## Contributing

Two things make a change easy to accept: keep the framework **universal** (no personal data, ever), and for a new model follow `Models/AGENT.md` — including a real falsification attempt. A failed falsification is a useful result; report it rather than dropping it.

## License

MIT — see [LICENSE](LICENSE).
