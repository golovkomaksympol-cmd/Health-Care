# _core — Shared Framework

Universal philosophy, models, and protocol templates applied to every patient in this repo (including the repo owner). Patient folders hold personal data and overrides; `_core/` holds the framework they extend.

## How the LLM should use _core/

For any patient query, load:
1. The relevant `_core/*.md` files (framework defaults).
2. The patient's `Medical Profile.md` and `Human Context.md` (personal data + overrides).

Patient overrides always win over `_core/` defaults. If a patient's Medical Profile says "iron protocol: heme + lactoferrin", that overrides whatever the framework suggests.

## File index

| File                            | Scope                                                                                                               |
| ------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| `meta-thinking.md`              | Answer-quality contract: anti-sycophancy, signal-vs-noise, attention gate, anti-patterns                             |
| `Health Philosophy.md`          | CEO mindset, Medicine 3.0, Four Horsemen, reverse engineering from age 90                                           |
| `Decision Principles.md`        | How to choose interventions (Optimal>Normal, signal-to-noise, hierarchy of controls, etc.)                          |
| `Operating Modes.md`            | Architect vs Operator mode, "mood follows metabolism"                                                               |
| `mentor-panel.md`               | The panel *method* + domain roster (per-person roster lives in the person's profile)                                |
| `Practices Framework.md`        | TOC bottleneck, Defcon levels, Impact/Friction scoring rubric                                                       |
| `Sleep Protocol.md`             | CBT-I template, sleep restriction, melatonin notes                                                                  |
| `Training Framework.md`         | Weekly skeleton, McGill Big 3+1, strength A/B split, Zone 2, Zone 5                                                 |
| `Exercise Catalog.md`           | Pick-list for `plan-workout`, grouped by movement pattern; equipment + flags                                        |
| `Nutrition Framework.md`        | Fasting window, protein targets, meal order, macro principles                                                       |
| `Daily Architecture.md`         | 4 phases of the day (load / perform / sync / dissolve)                                                              |
| `Meditation Framework.md`       | Concentration vs Clarity split; Culadasa/Shinzen; teacher-comment rubric                                            |
| `Relationships Framework.md`    | 4 levels (Self / Others / Work / Higher) with their Idols; Gottman, Dunbar, Tail End                                |
| `Sati (Re-reading Practice).md` | The meta-practice of regular re-reading to prevent config drift                                                     |
| `Onco Screening.md`             | Female + universal cancer screening; black list of low-value tests                                                  |
| `Trigger Diagnostics.md`        | Stage-2 if→then rules: which finding justifies which follow-up test, and when NOT to escalate                        |
| `Models/`                       | Mechanistic models that drive practices — universal causal chains (e.g. muscle hypertrophy). See `Models/AGENT.md`. |

**Not yet written** (referenced in places as future work, deliberately absent rather than stubbed): `Supplement Framework.md`, `HRT Framework (Female).md`. Until they exist, supplement stacks and HRT decisions live in each person's profile.

