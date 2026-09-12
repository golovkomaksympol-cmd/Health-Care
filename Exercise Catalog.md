# Exercise Catalog

Pick-list for the `plan-workout` skill. The agent **selects from here** (filtered by gym equipment + readiness + constraints), it does not invent exercises. Grouped by movement **pattern**. Power is sub-grouped by the ProPower pattern taxonomy (`_core/Models/ProPower (Power & RFD).md`).

**Legend**
- **Adaptation:** Str=strength · Pow=power · Hyp=hypertrophy · ME=muscular endurance · Stab=stability/core · Mob=mobility · Rehab
- **Equip:** BB=barbell · DB=dumbbell · KB=kettlebell · trap=trap-bar · mini=mini/EZ-bar · cable · mach=machine · BW=bodyweight · band · box · bench · rack · med=med-ball · wall
- **Flags:** `U`=unilateral · `spine⚠`=loaded spine → neutral/control (hypermobility) · `calf`=loads calf/Achilles · `ecc`=eccentric/CK-heavy (novel-load caution) · `skill`=high technique · `wall`=needs wall/partner/space to throw (impractical in a standard commercial gym) · `knee⚠(heavy)`=high patellofemoral pressure at heavy loads — light and terminal-range if the knee is irritable
- **Fam** (familiar) = already in **your** current repertoire → lower skill/injury risk than a novel movement. Mark these yourself with `✓`; the planner prefers them when readiness is low or a novel stimulus would stack risk. An empty column is fine — it just means "nothing marked yet".
- **🎥** = direct link to a curated form-reference clip for that exact movement. **A blank cell means no clip has been chosen yet** — don't fabricate a URL and don't substitute a search link; either leave it blank or tell the trainee to search the exercise name. The column fills in over time.
- **One row = one movement.** Don't merge two exercises into a row with a slash; give each its own row. A parenthetical is an alias for the *same* movement (e.g. `Plyo Push-up (clap)`), not a second exercise. One clip per row is the norm; a second is fine only when it covers the *same* movement from another angle.
- **Setup often matters as much as the exercise.** For many rows the same movement hits a different muscle depending on foot position, torso lean, grip or joint angle — see **[Variant selection](#variant-selection--where-the-setup-changes-the-target)** at the end of this file. When an exercise with variants is prescribed, the variant must be named.

> In-gym adaptations: Str, Pow, Hyp, ME, Stab. **Trained OUTSIDE the gym (not here):** VO₂max/Zone 5 (Norwegian), Zone 2 / long-duration (run), skill/gait (running technique), dance. See `Practices`.

## Index — finding an exercise by muscle

This catalog is grouped by **movement pattern**, not by muscle, because strength, power and skill adapt at the level of the pattern (`Training Adaptations (Galpin 9).md`, `ProPower (Power & RFD).md`). Hypertrophy is the exception — there the muscle *is* the unit (`Skeletal Muscle Hypertrophy.md`), so use this index when you're thinking in muscles.

**"Back" has no section of its own — it is split across three patterns.** That's the most common lookup failure:

| Looking for | Section(s) |
|---|---|
| **Lats** | Vertical pull · Horizontal pull |
| **Erectors / lower back** | **Hinge** — 45° Back Extension, Romanian Deadlift, Deadlift |
| **Traps / rhomboids / rear delt** | Horizontal pull · Isolation patches (Face Pulls) |
| Chest | Horizontal push |
| Shoulders (delts) | Vertical push · Isolation patches (Lateral Raises, Face Pulls) |
| Biceps | Vertical pull · Isolation patches |
| Triceps | Horizontal push (Dips) · Isolation patches |
| Quads | Squat · Unilateral lower |
| Hamstrings | Hinge |
| Glutes | Hip extension / glute · Hinge · Unilateral lower |
| Adductors | Unilateral lower (Cossack) · Knee/foot (Copenhagen) |
| Calves / Achilles | Calf / lower-leg |
| Abs / trunk | Core / anti-rotation · Carries |
| Grip | Carries |

## Squat (knee-dominant)
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Back Squat | quads, glutes, trunk | Str/Hyp | BB, rack | spine⚠ | | [🎥](https://www.youtube.com/shorts/tNUq6b5t11Q) |
| Front Squat | quads, trunk | Str/Hyp | BB, rack | spine⚠, skill | ✓ | [🎥](https://www.youtube.com/shorts/_qv0m3tPd3s) |
| Goblet Squat | quads, glutes | Hyp/ME | DB/KB | | ✓ | [🎥](https://www.youtube.com/shorts/ZBAd1g1z6qs) |
| Hack Squat | quads | Str/Hyp | mach | | ✓ | [🎥](https://www.youtube.com/shorts/cFGgMO-ENiQ) |
| Leg Press | quads, glutes | Str/Hyp | mach | | ✓ | [🎥](https://www.youtube.com/shorts/EotSw18oR9w) |
| Leg Extension | quads (isolation) | Hyp | mach | knee⚠(heavy) | ✓ | [🎥](https://www.youtube.com/shorts/iQ92TuvBqRo) |
| Belt Squat | quads, glutes — **no axial load** | Str/Hyp | belt-squat mach | | |  |

## Hinge (hip-dominant)
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Romanian Deadlift | hamstrings, glutes, erectors | Str/Hyp | BB/DB | spine⚠, ecc | ✓ | [🎥](https://www.youtube.com/shorts/QbbURJEUALw) |
| Conventional Deadlift | post chain, quads | Str | BB, rack | spine⚠ | | [🎥](https://www.youtube.com/shorts/K8a_Ab9R-aI) |
| Trap-bar Deadlift | post chain, quads | Str | trap | spine⚠ | ✓ |  |
| Single-leg RDL | hamstring, glute, balance | Hyp/Stab | DB/KB | U, ecc | |  |
| 45° Back Extension | erectors, glutes, hams | Hyp/ME | mach/+plate | spine⚠ | ✓ |  |
| Leg Curl (seated preferred) | hamstrings (knee flexion) | Hyp | mach | | ✓ |  |
| Reverse Hyper | glutes, hamstrings → erectors via hip extension, torso fixed | Hyp/Rehab | reverse-hyper mach | | |  |

## Hip extension / glute (patterning)
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Machine Hip Thrust (Glute Drive) | glute max | Str/Hyp | mach | | ✓ | [🎥](https://www.youtube.com/shorts/2jFSouNMeS4) |
| Single-leg Glute Bridge | glute max (timing) | Stab/Hyp | BW/band | U | |  |
| Banded Glute Bridge | glute activation | Stab/activation | band | | |  |
| Clamshell | glute med (pelvic stab) | Stab/activation | band | | |  |
| Lateral Band Walk | glute med (pelvic stab) | Stab/activation | band | | |  |
| Cable Glute Kickback | glute max | Hyp | cable | U | |  |
| Hip Abduction | glute med | Hyp | mach | | ✓ |  |
| Hip Adduction | adductors | Hyp | mach | | ✓ |  |
| Step-up | glute, quad, drive | Str/Hyp | DB/box | U, calf | |  |
| Hip Airplane | glute + rotational stability | Stab | BW | U, skill | |  |

## Unilateral lower / lunge
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Bulgarian Split Squat | quad, glute | Str/Hyp | DB/KB | U, ecc | ✓ | [🎥](https://www.youtube.com/shorts/or1frhkjBDc) |
| Reverse Lunge | quad, glute | Hyp | DB | U | |  |
| Cossack Squat | adductors, mobility, lateral stability | Stab/Mob | BW/light | U | ✓ | [🎥](https://www.youtube.com/shorts/TR4GN3rLuQ8) |

## Horizontal push
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Barbell Bench Press | chest, triceps, front delt | Str/Hyp | BB, bench, rack | | ✓ | [🎥](https://www.youtube.com/shorts/XjrsqShr-Ic) |
| Incline Bench Press | upper chest, triceps | Str/Hyp | BB, bench | | ✓ | [🎥](https://www.youtube.com/shorts/Uf2To5LoYBE) |
| Incline DB Press | upper chest | Hyp/Str | DB, bench | | ✓ |  |
| Seated Machine (Incline) Press | chest | Hyp | mach | | ✓ |  |
| Dips (parallel bar) | lower chest, triceps | Str/Hyp | BW/+weight, bar | | ✓ | |
| Bench Dips | triceps | Hyp | bench, BW | | | [🎥](https://www.youtube.com/shorts/cFK5G2Exwwo) |
| Seated Dip Machine | triceps, lower chest | Hyp | mach | | |  |
| Chest Press (machine) | chest, triceps | Hyp/Str | mach | | ✓ |  |

## Vertical push
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Overhead Press (BB) | delts, triceps, trunk | Str/Hyp | BB/mini, rack | spine⚠(overhead) | ✓ | [🎥](https://www.youtube.com/shorts/4LBVP2Oe7fg) [🎥](https://www.youtube.com/shorts/zoN5EH50Dro) |
| DB Shoulder Press | delts | Hyp/Str | DB | | ✓ | [🎥](https://www.youtube.com/shorts/k6tzKisR3NY) |
| Machine Shoulder Press (converging) | delts | Hyp/Str | mach | | |  |

## Horizontal pull
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Barbell Bent-Over Row | lats, rhomboids, erectors | Str/Hyp | BB | spine⚠ | ✓ | [🎥](https://www.youtube.com/shorts/phVtqawIgbk) |
| Seated Cable Row | lats, mid-back | Str/Hyp | cable/mach | | ✓ | [🎥](https://www.youtube.com/shorts/LyZH4UGdDTc) |
| Dual Pulley Row | lats, mid-back | Str/Hyp | cable | | ✓ |  |
| Chest-supported Row (machine) | mid-back (no spine load) | Hyp | mach | | | [🎥](https://www.youtube.com/shorts/G35gTqGcXXA) |

## Vertical pull
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Pull-up | lats, biceps | Str/Hyp | BW, bar | | ✓ | [🎥](https://www.youtube.com/shorts/HmVIu6OEsv4) |
| Weighted Pull-up | lats, biceps | Str | +weight, bar | | ✓ |  |
| Lat Pulldown | lats | Hyp/Str | cable/mach | | ✓ | [🎥](https://www.youtube.com/shorts/bNmvKpJSWKM) |

---

## POWER / explosive — do FIRST, fresh, low reps (1–5), max intent, NOT to failure
Sub-grouped by ProPower pattern. **Transfer is narrow — train the pattern you need** (`ProPower (Power & RFD).md`). Pick a pattern **not** hit recently to broaden the vector.

### Vertical push / triple-extension-up
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Push Press | explosive vertical push (leg drive→overhead) | Pow/Str | BB/DB | skill | ✓ |  |
| Jump Squat (light) | lower explosive | Pow | BW/light | calf, ecc | |  |
| Box Jump | lower-body explosive + vertical | Pow | box | calf | ✓ |  |
| Trap-bar Jump | total-body explosive (loaded) | Pow | trap | calf, skill | |  |

### Hinge / posterior ballistic
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Kettlebell Swing | posterior chain (hip power) | Pow | KB | | ✓ | [🎥](https://www.youtube.com/shorts/3lMRRqyTuK8) |
| Power Clean | total posterior explosive | Pow | BB | skill | |  |
| Broad Jump | horizontal hip explosive | Pow | BW | calf, ecc | |  |

### Horizontal push
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Plyo Push-up (clap) | explosive horizontal push | Pow | BW | | |  |
| Med-ball Chest Pass | explosive horizontal push | Pow | med, wall | wall | |  |
| Speed Bench (~50–60%) | RFD on the bench pattern | Pow | BB, bench | | |  |

### Horizontal / vertical pull (explosive)
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Barbell High Pull | explosive pull (traps, posterior) | Pow | BB | skill | |  |
| Speed Row (~50–60%) | RFD on the row pattern | Pow | BB/cable | | |  |

### Rotation (no wall needed → cable)
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Explosive Cable Rotation | rotational power (hips→trunk) | Pow | cable | | ✓(rotation) |  |
| Cable Chop (fast) | diagonal rotational power | Pow | cable | | |  |
| Med-ball Rotational Throw | rotational power | Pow | med, wall | wall | |  |

### Locomotor / reactive (SSC-dominant)
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Pogo Hops | ankle stiffness / reactive | Pow | BW | calf | |  |
| Bounding | reactive horizontal | Pow | BW | calf, ecc | |  |
| Skater Bounds | reactive lateral | Pow | BW | calf, ecc | | [🎥](https://www.youtube.com/shorts/IkGOdk2VDJw) |
| Depth Jump | reactive SSC (advanced) | Pow | box | calf, ecc, skill | |  |

### Landing / deceleration (eccentric power — the neglected one)
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Drop Landing (stick the landing) | eccentric absorb / fall-arrest | Pow | box/BW | calf, ecc | |  |
| Snap-down | rapid deceleration / athletic position | Pow | BW | | |  |

### Speed reps (RFD on the main lifts)
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Speed reps (squat/bench/pull ~50–60%) | RFD on a main lift | Pow | BB | | |  |

---

## Carries (anti-lateral-flexion / grip / trunk — Core Stability)
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Suitcase Carry | obliques/QL (anti-lat-flex) | Stab/ME | DB/KB | U, calf | ✓ |  |
| Farmer Carry | grip, trunk, total | Stab/ME | DB/KB/trap | calf | |  |
| Front-rack Carry | anti-extension, trunk | Stab | KB/DB | calf | |  |
| Overhead Carry | shoulder stab, anti-extension | Stab | KB/DB | calf | |  |
| Bottom-up KB Carry | grip + shoulder stability | Stab | KB | U | ✓ |  |

## Core / anti-rotation / stability (Core Stability model)
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| McGill Curl-up | anti-extension (anterior core) | Stab | BW | | |  |
| Side Plank | anti-lateral-flexion (QL/obliques) | Stab | BW | | |  |
| Bird Dog | anti-rotation, spinal control | Stab | BW | | |  |
| Pallof Press | anti-rotation | Stab | cable/band | | |  |
| Dead Bug | anti-extension, coordination | Stab | BW | | |  |
| Standing Cable Rotation | rotation control | Stab/Hyp | cable | | ✓ |  |
| Hanging Leg Raise | hip flexors, rectus | Hyp/ME | bar/+ball or DB | spine⚠(flexion) | ✓ |  |
| Decline Crunch | rectus (dynamic flexion) | Hyp/ME | bench/+plate | spine⚠(flexion) | ✓ |  |
| Russian Twist | obliques (rotation) | Hyp/ME | bench/+plate | spine⚠(flexion) | ✓ |  |

## Calf / lower-leg (rehab + tolerance)
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Single-leg Heel Raise (Alfredson, eccentric) | gastroc/soleus + Achilles | Rehab/Str | BW/step | U, calf | ✓ |  |
| Standing Calf Raise | gastrocnemius (knee straight) | Hyp | mach/DB | calf | | [🎥](https://www.youtube.com/shorts/a-x_NR-ibos) |
| Seated Calf Raise | soleus (knee bent) | Hyp | mach | calf | |  |

## Isolation patches (weak-link fillers)
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Lateral Raises | side delts | Hyp | DB/cable | | ✓ | [🎥](https://www.youtube.com/shorts/lMYs7FY8os4) [🎥](https://www.youtube.com/shorts/Kl3LEzQ5Zqs) |
| Face Pulls | rear delts, shoulder health | Hyp/Stab | cable/band | | ✓ | [🎥](https://www.youtube.com/shorts/YjOb2nFvFy0) |
| Rear-delt Pec Deck (reverse fly) | rear delts, rhomboids | Hyp | mach | | |  |
| Biceps Curl | biceps | Hyp | DB/BB/mini | | ✓ | [🎥](https://www.youtube.com/shorts/MKWBV29S6c0) |
| Triceps Pushdown | triceps | Hyp | cable | | ✓ | [🎥](https://www.youtube.com/shorts/d9l2AYTGIEs) |

## Knee / foot (rehab & control — FEEL dose, never near failure)
Load-related knee pain (patellofemoral, ITB) responds to **hip and quad control**, not to "knee exercises" as such — so frontal-plane glute work belongs to this block too (rows in **Hip extension / glute**). Isometrics are the analgesic entry on the loading ladder. Foot/toe work is about **loading the first ray properly**; a callus is a friction sign, so **check shoe fit before blaming the muscles**.

| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Spanish Squat | quad isometric, knee-friendly | Rehab/Str | band, rack | | | [🎥](https://www.youtube.com/shorts/lqAh-DpfoZA) |
| Step-down (controlled) | knee control in the frontal plane | Rehab/Stab | box/step | U, ecc | |  |
| Terminal Knee Extension (TKE) | vastus medialis, end-range knee ext | Rehab | band | | |  |
| Wall Sit | quad isometric (analgesic) | Rehab/ME | BW | | |  |
| Copenhagen Plank | adductors, pelvic control | Stab | bench | U, ecc | |  |
| BlackBoard — hallux dorsiflexion | big-toe extensors, first-ray control | Rehab/Stab | BlackBoard | U, skill | |  |
| BlackBoard — hallux plantarflexion | flexor hallucis, first-ray load | Rehab/Stab | BlackBoard | U, skill | |  |
| Short Foot (arch doming) | intrinsic foot muscles | Rehab/Stab | BW | U, skill | |  |
| Toe Splay / Spread | toe abductors, forefoot width | Rehab/Mob | BW/spacers | | |  |

> **Dosing:** these are **FEEL** work — deliberately submaximal, high quality, repeatable near-daily. Taking them near failure converts them to LOOK work and destroys the frequency that makes them work. Enter at the step of the loading ladder you can own: isometric → anti-movement + fatigue → anti-movement + load → movement + fatigue → movement + load. **Introduce one novel item at a time** (`ecc`/`skill` flags stack badly).

## Mobility / activation (warm-up; Cook readiness)
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Couch Stretch (hip flexor) | hip flexors (unblock glute) | Mob | BW | | |  |
| Hip 90/90 | hip rotation mobility | Mob | BW | | ✓ |  |

> **Glute activation priming** (Banded Glute Bridge, Clamshell, Lateral Band Walk) lives in **Hip extension / glute** above — use those rows rather than duplicating them here.

---

---

## Machine notes — what each machine does well, where it bites, and the cue

Source: Jeff Cavaliere's machine ranking (ATHLEAN-X, [video](https://youtu.be/x9jvUHbbIhU)), **re-weighed** rather than copied. His ranking optimises for shoulder/lumbar safety and hypertrophy from a physio's chair — mostly sound biomechanics, a few stylistic preferences. Two corrections for a **lax-tissue / control-limited trainee** (`Models/Core Stability.md`): (1) his "natural movement is always better" downgrades fixed-path machines, but when *control* is the limiter a fixed path is sometimes exactly the point; (2) any cue that adds torso motion under load (swinging on a row, hips driving on a curl) counts against, not for. Nothing here is removed from the catalog — these are the trade-offs to name when prescribing.

| Machine | Good for | Where it bites | Cue / when to prefer it | Verdict |
|---|---|---|---|---|
| **Leg Curl — lying** | hamstring isolation | prone with hips flat → hamstring shortens at both joints (active insufficiency), hips lift, **lumbar extension under load** | angled pad (hips ~30°) fixes most of it; otherwise choose seated | avoid if a seated one exists |
| **Leg Curl — seated** | hamstring at **long length** — more growth than prone in a direct comparison (Maeo 2021); hip flexors and lumbar out of the movement | none of note | lower with two legs, lift with one for controlled overload | **preferred** |
| **Hip Abduction / Adduction (seated)** | targeted glute-med (abd) and adductor (add) loading with **full control of load and range** | seated is not the functional plane; "builds glutes" is glute *med*, not max (see Variant selection) | upright → glute med; **for a frontal-plane control deficit this is the *load* tool** — band walks / lateral lunges are the *control* tool; use both, don't swap one for the other | keep; Cavaliere over-downgrades it |
| **Lateral Raise machine** | strict path | pads fix the forearm → shoulder can't rotate out → impingement-prone at the top | DB or cable with **thumb slightly above pinky** | prefer DB/cable |
| **Preacher Curl (flat pad)** | biceps at long length | elbow becomes a rigid fulcrum, distal tendon exposed at heavy loads | choose a pad that slopes away; standing with elbows braced is fine | caution |
| **Chest Fly machine (pec deck, chest)** | pec adduction | fixed arc; start position can **overstretch the anterior capsule** if arm span doesn't match | set the start inside your range, not at the machine's | caution; cable crossover is the same movement without the fixed arc |
| **Chest-supported Row** | mid-back with **zero spinal load** — the go-to when the back or neck is irritated | the chest pad tends to round the shoulders forward | chest lifts off the pad slightly, glutes lightly tensed on the prone version | **good** |
| **Seated Dip machine** | triceps/lower chest when the shoulder girdle shouldn't take body weight (bar dips off the table) | — | arms travel slightly behind the torso → long head | good alternative to bar dips |
| **Leg Press** | quad loading with a supported back; controlled ROM — the **return-from-injury** tool | no full hip extension → glutes under-stimulated; heavy loads shift to ligaments; not a squat replacement | feet high → less knee, more hip; treat as a supplement | good, with the caveat |
| **Smith machine** | spotter-free pressing | fixed bar path forces the body to fit the machine; squat ankle mechanics distorted; **balance is taken over, so the number lies** | pressing yes; squatting only if nothing else | caution |
| **Machine Shoulder Press (converging)** | wrist–elbow–shoulder in one line; **no standing lumbar extension** | — | sit **2 cm off the backrest** so the scapulae can move | **very good** — the overhead choice when the neck or low back is irritable |
| **Rear-delt Pec Deck** | rear delt / rhomboids **seated** — removes the lumbar lean-back that standing face pulls invite | entering/exiting the handles can jar the shoulder | turn the torso, take one handle, then the other | **very good** |
| **Chest Press machine** | elbows guided to ~45–60° — shoulder-friendly; safe to take to fatigue alone | — | — | **very good** |
| **Leg Extension** | pure quad isolation; the only way to load quads with zero hip or spine involvement | **high patellofemoral pressure at heavy loads** (peak in the 90→45° range) | irritable knee → light load, **terminal range 0–40°**, rehab tempo; reclined seat → rectus femoris, upright → vasti | good, dose it |
| **Hack Squat** | angled platform helps ankle dorsiflexion; back supported; good front-squat alternative when wrists/thoracic limit the barbell | still axial load through the shoulders | feet high on the platform → less knee | **good** |
| **Reverse Hack** | forward lean → glutes | no final hip extension | pair with a full-extension movement (hip thrust) | ok |
| **Functional trainer / cables** | any natural path, adjustable to your anatomy; ideal for rotation, Pallof, face pulls | needs a little skill to aim the cable | — | **very good** |
| **Viking / landmine press** | standing press with neutral grip and a **forward-angled path** — less lumbar extension than a strict overhead bar, scapulae free | needs the implement | — | good overhead alternative |
| **Seated Cable Row** | free torso — but see the correction | Cavaliere cues torso swing "to open the chest"; **for a lax spine that swing is lumbar flexion/extension under load** | torso still, ribs down; elbows low and tucked → lats, high and wide → upper back | good — **with a still torso** |
| **Belt Squat** | **removes spinal compression entirely**; pelvis sits into a good position; full squat pattern | rare in commercial gyms | hands may assist heavy reps | **the squat of choice during any back episode** |
| **Standing Calf Raise** | heavy gastrocnemius loading | the Achilles spring hides the muscle work | **4 s pause at the bottom** removes the stretch-shortening rebound | good |
| **Cable Crossover** | full pec adduction in a safe stretch | — | high→low for lower chest, low→high for upper | good |
| **Lat Pulldown** | dosable vertical pull when pull-ups are too much or too few | — | vary grips (see Variant selection) | **very good** |
| **Reverse Hyper** | erector work **through hip extension with the torso fixed** — no axial compression, rhythmic lumbar decompression | evidence is mechanistic and anecdotal (no trials); rare machine | light, rhythmic, high reps | good when available — candidate for an extension-preference back |
| **Hip Thrust machine** | resistance exactly at full hip extension — the one thing squats can't give; easy to set up, no bar on the pelvis | slow eccentrics hold the knee at ~90° under load → patellofemoral cost if the knee is irritable | shin vertical at lockout; ribs down; **normal tempo** | **very good** |

---

## Variant selection — where the setup changes the target

Same exercise, different setup → **different muscle does the work**. When an exercise below is prescribed, the plan must name **which variant and why** (see the `plan-workout` skill). Default rule: pick the variant that hits the pattern the session is *for*, and avoid the variant that doubles a muscle already loaded elsewhere that day.

**What's real vs what's marketing.** The shifts listed here work through **joint angle → muscle length and moment arm** (knee angle, torso lean, foot position, where the arm sits relative to the torso). Those are mechanical and reliable. Claims about steering load *within* one muscle head — "inner/outer chest", biceps "peak", toe angle for quad "sweep" — are **not** reliable; they aren't in this table.

### Lower body
| Exercise | What you change | Variant → emphasis |
|---|---|---|
| Back Squat | bar position / stance | high-bar + upright → **quads**; low-bar + more hip hinge → **glutes + posterior chain**; wide stance → **adductors/glutes**; heels elevated → **quads** |
| Leg Press · Hack Squat | foot placement on platform | low on platform → **quads**; high → **glutes + hamstrings**; wide + toes out → **adductors/glutes** |
| Leg Extension | seat/hip angle | reclined (hip open) → **rectus femoris** at long length; upright → **vasti** |
| Romanian Deadlift | knee angle / stance | stiffer knee, less hip travel → **hamstrings**; softer knee, more hip travel → **glutes**; wide stance → **adductors/glutes** |
| Trap-bar Deadlift | handle height | high handles → shorter ROM, **more quad**, less lower-back; low handles → closer to conventional, **hamstrings/erectors** |
| 45° Back Extension | spine + pelvis | neutral spine, posterior pelvic tilt, toes out → **glutes**; spine flexing/extending through the rep → **erectors** |
| Leg Curl | hip position / ankle | seated (hip flexed → hamstring stretched) → stronger **long-length hamstring** stimulus; lying → shortened; ankle dorsiflexed → adds **gastrocnemius** |
| Machine Hip Thrust | foot position at lockout | shin **vertical** → **glute max**; feet closer to hips → **quads**; feet further forward → **hamstrings**; wider + toes out → more **upper glute / glute med** |
| Cable Glute Kickback | knee angle | knee held bent → isolates **glute max**; straight leg → adds **hamstring** |
| Hip Abduction (machine) | torso angle | leaned forward → **upper glute max**; upright/leaned back → **glute medius** |
| Step-up | box height / torso | higher box + forward lean → **glutes**; lower box + upright → **quads** |
| Bulgarian Split Squat | torso + front-foot distance | upright, foot closer → **quads**; leaned forward, foot further → **glutes/hamstrings** |
| Reverse Lunge | step length | short step → **quads**; long step → **glutes/hamstrings** |
| Cossack Squat | rep style · counterweight | **rocking** (stay low, shift side to side, never stand up) → **mobility / adductor range**, warm-up tool; **full reps** (stand between sides) → **strength + frontal-plane control** on the working leg. A **counterweight held at the chest** (goblet KB/DB, 8–12 kg) is a *technique* tool before it is load — it lets you sit back further with an upright torso, so depth and heel contact improve. Depth is capped by **neutral spine and a flat working heel**, never by how low you can get |
| Standing vs Seated Calf Raise | knee angle | knee **straight** → **gastrocnemius**; knee **bent** → **soleus** (this is why both rows exist; Alfredson uses both) |

### Upper body — push
| Exercise | What you change | Variant → emphasis |
|---|---|---|
| Bench / Incline Press | bench angle · grip width | flat → **mid pec**; 15–30° → **upper (clavicular) pec**; >45° drifts to **anterior delt**; wider grip → **pec**; narrower → **triceps** |
| Dips | torso lean · elbow path | leaned forward, elbows out → **chest**; upright, elbows tucked → **triceps** |
| Overhead Press (BB) | standing vs seated | standing → whole-body/**trunk** demand, less load; seated → more isolated **delts**, heavier possible. *Behind-the-neck: skip — shoulder risk, worse with hypermobility.* |
| DB Shoulder Press | grip | neutral/hammer → **anterior delt**, shoulder-friendlier; pronated → slightly more **lateral delt** |
| Lateral Raises | torso angle · cable-lean vs dumbbell | torso **upright** → **lateral delt**; torso leaned **forward** ~30° → the resistance vector moves behind the shoulder → **posterior delt** (a different exercise, not a "better feel"). Leaning away on a cable → tension in the **stretched** position; dumbbell → tension at the **top** |
| Triceps | arm position | overhead extension → **long head** (stretched); pushdown → **lateral/medial heads** |

### Upper body — pull
| Exercise | What you change | Variant → emphasis |
|---|---|---|
| Barbell Row · Seated Cable Row | elbow path · grip · torso angle | elbows tucked ~45°, underhand/neutral → **lats**; elbows flared ~90°, wide overhand → **rear delts, rhomboids, traps**; torso more horizontal → **mid-back**; more upright → **upper traps** |
| Pull-up · Lat Pulldown | grip | wide pronated → **lats**, least biceps; supinated (chin-up) → **biceps + lower lats**; neutral → **brachialis**, easiest on shoulder/elbow. Leaning back ~30° on the pulldown turns it into a **row (mid-back)** |
| Biceps Curl | where the arm sits | incline, arm behind torso → **long head** at long length; preacher, arm in front → **short head**; hammer/neutral → **brachialis + brachioradialis** |

### Power
| Exercise | What you change | Variant → emphasis |
|---|---|---|
| Kettlebell Swing | swing height | **Russian** (to chest/eye level) → **hip power** — this is the one the ProPower model wants; **American** (overhead) adds shoulder demand + lumbar extension → **skip with `spine⚠` / hypermobility** |
| Push Press vs Overhead Press | leg drive | with leg drive → **power (RFD)**; strict → **shoulder strength** |
| Skater Bounds · Bounding · Pogo Hops | what you do with the landing | **stick it** (land, freeze ~1 s, other foot never touches) → **eccentric deceleration + frontal-plane control**; **bounce off it** (shortest possible ground contact) → **reactive SSC / stiffness**. Two different adaptations from one movement — pick one per set, don't blend. Progress the stick version by **distance**, the bounce version by **contact time**. Height is not a variable in either — it only raises landing force |

### Core / carries
| Exercise | What you change | Variant → emphasis |
|---|---|---|
| Carries | how the weight is held | **the position *is* the variant** — suitcase (one side) → **anti-lateral-flexion**; farmer (both) → **grip + trunk**; front-rack → **anti-extension + thoracic**; overhead → **shoulder stability**; bottom-up → **grip + cuff/shoulder control** |
| Pallof Press | stance · distance from anchor | half-kneeling → removes leg drive, harder on the **trunk**; split stance → adds **hip stability**; further from the anchor → longer lever, harder |
| Side Plank | base of support | from knees → regression; feet stacked → full; top leg forward → wider base, easier |
| Hanging Leg Raise | where the movement happens | legs raised with a **neutral pelvis** (stop at hip height) → **hip flexors**, minimal spinal load; **posterior pelvic tilt / curling the pelvis up** at the top → **rectus abdominis**, but that's the loaded-flexion part — regress it under `spine⚠`. Bent knees → regression; straight legs or a load between the feet → progression |
| Standing Cable Rotation | hips locked or free | hips locked → **trunk rotation control**; hips free → **whole-body rotational power** |
