# Exercise Catalog

Pick-list for the `plan-workout` skill. The agent **selects from here** (filtered by gym equipment + readiness + constraints), it does not invent exercises. Grouped by movement **pattern**. Power is sub-grouped by the ProPower pattern taxonomy (`_core/Models/ProPower (Power & RFD).md`).

**Legend**
- **Adaptation:** Str=strength · Pow=power · Hyp=hypertrophy · ME=muscular endurance · Stab=stability/core · Mob=mobility · Rehab
- **Equip:** BB=barbell · DB=dumbbell · KB=kettlebell · trap=trap-bar · mini=mini/EZ-bar · cable · mach=machine · BW=bodyweight · band · box · bench · rack · med=med-ball · wall
- **Flags:** `U`=unilateral · `spine⚠`=loaded spine → neutral/control (hypermobility) · `calf`=loads calf/Achilles · `ecc`=eccentric/CK-heavy (novel-load caution) · `skill`=high technique · `wall`=needs wall/partner/space to throw (impractical in a standard commercial gym)
- **Fam** (familiar) = already in **your** current repertoire → lower skill/injury risk than a novel movement. Mark these yourself with `✓`; the planner prefers them when readiness is low or a novel stimulus would stack risk. An empty column is fine — it just means "nothing marked yet".
- **🎥** = direct link to a curated form-reference clip for that exact movement. **A blank cell means no clip has been chosen yet** — don't fabricate a URL and don't substitute a search link; either leave it blank or tell the trainee to search the exercise name. The column fills in over time.
- **One row = one movement.** Don't merge two exercises into a row with a slash; give each its own row. A parenthetical is an alias for the *same* movement (e.g. `Plyo Push-up (clap)`), not a second exercise. One clip per row is the norm; a second is fine only when it covers the *same* movement from another angle.
- **Setup often matters as much as the exercise.** For many rows the same movement hits a different muscle depending on foot position, torso lean, grip or joint angle — see **[Variant selection](#variant-selection--where-the-setup-changes-the-target)** at the end of this file. When an exercise with variants is prescribed, the variant must be named.

> In-gym adaptations: Str, Pow, Hyp, ME, Stab. **Trained OUTSIDE the gym (not here):** VO₂max/Zone 5 (Norwegian), Zone 2 / long-duration (run), skill/gait (running technique), dance. See `Practices`.

## Squat (knee-dominant)
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Back Squat | quads, glutes, trunk | Str/Hyp | BB, rack | spine⚠ | | [🎥](https://www.youtube.com/shorts/tNUq6b5t11Q) |
| Front Squat | quads, trunk | Str/Hyp | BB, rack | spine⚠, skill | ✓ | [🎥](https://www.youtube.com/shorts/_qv0m3tPd3s) |
| Goblet Squat | quads, glutes | Hyp/ME | DB/KB | | ✓ | [🎥](https://www.youtube.com/shorts/ZBAd1g1z6qs) |
| Hack Squat | quads | Str/Hyp | mach | | ✓ | [🎥](https://www.youtube.com/shorts/cFGgMO-ENiQ) |
| Leg Press | quads, glutes | Str/Hyp | mach | | ✓ | [🎥](https://www.youtube.com/shorts/EotSw18oR9w) |
| Leg Extension | quads (isolation) | Hyp | mach | | ✓ | [🎥](https://www.youtube.com/shorts/iQ92TuvBqRo) |

## Hinge (hip-dominant)
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Romanian Deadlift | hamstrings, glutes, erectors | Str/Hyp | BB/DB | spine⚠, ecc | ✓ | [🎥](https://www.youtube.com/shorts/QbbURJEUALw) |
| Conventional Deadlift | post chain, quads | Str | BB, rack | spine⚠ | | [🎥](https://www.youtube.com/shorts/K8a_Ab9R-aI) |
| Trap-bar Deadlift | post chain, quads | Str | trap | spine⚠ | ✓ |  |
| Single-leg RDL | hamstring, glute, balance | Hyp/Stab | DB/KB | U, ecc | |  |
| 45° Back Extension | erectors, glutes, hams | Hyp/ME | mach/+plate | spine⚠ | ✓ |  |
| Leg Curl | hamstrings (knee flexion) | Hyp | mach | | ✓ |  |

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
| Cossack Squat | adductors, mobility, lateral stability | Stab/Mob | BW/light | U | ✓ |  |

## Horizontal push
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Barbell Bench Press | chest, triceps, front delt | Str/Hyp | BB, bench, rack | | ✓ | [🎥](https://www.youtube.com/shorts/XjrsqShr-Ic) |
| Incline Bench Press | upper chest, triceps | Str/Hyp | BB, bench | | ✓ | [🎥](https://www.youtube.com/shorts/Uf2To5LoYBE) |
| Incline DB Press | upper chest | Hyp/Str | DB, bench | | ✓ |  |
| Seated Machine (Incline) Press | chest | Hyp | mach | | ✓ |  |
| Dips (parallel bar) | lower chest, triceps | Str/Hyp | BW/+weight, bar | | ✓ | |
| Bench Dips | triceps | Hyp | bench, BW | | | [🎥](https://www.youtube.com/shorts/cFK5G2Exwwo) |

## Vertical push
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Overhead Press (BB) | delts, triceps, trunk | Str/Hyp | BB/mini, rack | spine⚠(overhead) | ✓ | [🎥](https://www.youtube.com/shorts/4LBVP2Oe7fg) [🎥](https://www.youtube.com/shorts/zoN5EH50Dro) |
| DB Shoulder Press | delts | Hyp/Str | DB | | ✓ |  |

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
| Skater Bounds | reactive lateral | Pow | BW | calf, ecc | |  |
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
| Standing vs Seated Calf Raise | knee angle | knee **straight** → **gastrocnemius**; knee **bent** → **soleus** (this is why both rows exist; Alfredson uses both) |

### Upper body — push
| Exercise | What you change | Variant → emphasis |
|---|---|---|
| Bench / Incline Press | bench angle · grip width | flat → **mid pec**; 15–30° → **upper (clavicular) pec**; >45° drifts to **anterior delt**; wider grip → **pec**; narrower → **triceps** |
| Dips | torso lean · elbow path | leaned forward, elbows out → **chest**; upright, elbows tucked → **triceps** |
| Overhead Press (BB) | standing vs seated | standing → whole-body/**trunk** demand, less load; seated → more isolated **delts**, heavier possible. *Behind-the-neck: skip — shoulder risk, worse with hypermobility.* |
| DB Shoulder Press | grip | neutral/hammer → **anterior delt**, shoulder-friendlier; pronated → slightly more **lateral delt** |
| Lateral Raises | cable/lean vs dumbbell | leaning away on a cable → tension in the **stretched** position; dumbbell → tension at the **top** |
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

### Core / carries
| Exercise | What you change | Variant → emphasis |
|---|---|---|
| Carries | how the weight is held | **the position *is* the variant** — suitcase (one side) → **anti-lateral-flexion**; farmer (both) → **grip + trunk**; front-rack → **anti-extension + thoracic**; overhead → **shoulder stability**; bottom-up → **grip + cuff/shoulder control** |
| Pallof Press | stance · distance from anchor | half-kneeling → removes leg drive, harder on the **trunk**; split stance → adds **hip stability**; further from the anchor → longer lever, harder |
| Side Plank | base of support | from knees → regression; feet stacked → full; top leg forward → wider base, easier |
| Standing Cable Rotation | hips locked or free | hips locked → **trunk rotation control**; hips free → **whole-body rotational power** |
