# Exercise Catalog

Pick-list for the `plan-workout` skill. The agent **selects from here** (filtered by gym equipment + readiness + constraints), it does not invent exercises. Grouped by movement **pattern**. Power is sub-grouped by the ProPower pattern taxonomy (`_core/Models/ProPower (Power & RFD).md`).

**Legend**
- **Adaptation:** Str=strength · Pow=power · Hyp=hypertrophy · ME=muscular endurance · Stab=stability/core · Mob=mobility · Rehab
- **Equip:** BB=barbell · DB=dumbbell · KB=kettlebell · trap=trap-bar · mini=mini/EZ-bar · cable · mach=machine · BW=bodyweight · band · box · bench · rack · med=med-ball · wall
- **Flags:** `U`=unilateral · `spine⚠`=loaded spine → neutral/control (hypermobility) · `calf`=loads calf/Achilles · `ecc`=eccentric/CK-heavy (novel-load caution) · `skill`=high technique · `wall`=needs wall/partner/space to throw (impractical in a standard commercial gym)
- **Fam** (familiar) = already in **your** current repertoire → lower skill/injury risk than a novel movement. Mark these yourself with `✓`; the planner prefers them when readiness is low or a novel stimulus would stack risk. An empty column is fine — it just means "nothing marked yet".
- **🎥** = form reference. **Being migrated from channel-searches to direct clips** — a `youtube.com/shorts/…` or `watch?v=…` link is a curated video for that exact movement; a `@DeltaBolic/search?query=…` link is still a fallback search and **may return nothing** (especially for power/plyometric moves — jumps, swings, throws, bounds — which that channel doesn't cover). Use a general YouTube search when a fallback comes up empty.
- **One row = one movement = one video.** Don't merge two exercises into a row with a slash; give each its own row. A parenthetical is an alias for the *same* movement (e.g. `Plyo Push-up (clap)`), not a second exercise.

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
| Romanian Deadlift | hamstrings, glutes, erectors | Str/Hyp | BB/DB | spine⚠, ecc | ✓ | [🎥](https://www.youtube.com/@DeltaBolic/search?query=romanian+deadlift) |
| Conventional Deadlift | post chain, quads | Str | BB, rack | spine⚠ | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=conventional+deadlift) |
| Trap-bar Deadlift | post chain, quads | Str | trap | spine⚠ | ✓ | [🎥](https://www.youtube.com/@DeltaBolic/search?query=trap+bar+deadlift) |
| Single-leg RDL | hamstring, glute, balance | Hyp/Stab | DB/KB | U, ecc | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=single+leg+rdl) |
| 45° Back Extension | erectors, glutes, hams | Hyp/ME | mach/+plate | spine⚠ | ✓ | [🎥](https://www.youtube.com/@DeltaBolic/search?query=back+extension) |
| Leg Curl | hamstrings (knee flexion) | Hyp | mach | | ✓ | [🎥](https://www.youtube.com/@DeltaBolic/search?query=leg+curl) |

## Hip extension / glute (patterning)
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Machine Hip Thrust (Glute Drive) | glute max | Str/Hyp | mach | | ✓ | [🎥](https://www.youtube.com/@DeltaBolic/search?query=hip+thrust) |
| Single-leg Glute Bridge | glute max (timing) | Stab/Hyp | BW/band | U | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=single+leg+glute+bridge) |
| Banded Glute Bridge | glute activation | Stab/activation | band | | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=banded+glute+bridge) |
| Clamshell | glute med (pelvic stab) | Stab/activation | band | | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=clamshell) |
| Lateral Band Walk | glute med (pelvic stab) | Stab/activation | band | | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=lateral+band+walk) |
| Cable Glute Kickback | glute max | Hyp | cable | U | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=cable+glute+kickback) |
| Hip Abduction | glute med | Hyp | mach | | ✓ | [🎥](https://www.youtube.com/@DeltaBolic/search?query=hip+abduction+machine) |
| Hip Adduction | adductors | Hyp | mach | | ✓ | [🎥](https://www.youtube.com/@DeltaBolic/search?query=hip+adduction+machine) |
| Step-up | glute, quad, drive | Str/Hyp | DB/box | U, calf | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=step+up) |
| Hip Airplane | glute + rotational stability | Stab | BW | U, skill | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=hip+airplane) |

## Unilateral lower / lunge
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Bulgarian Split Squat | quad, glute | Str/Hyp | DB/KB | U, ecc | ✓ | [🎥](https://www.youtube.com/@DeltaBolic/search?query=bulgarian+split+squat) |
| Reverse Lunge | quad, glute | Hyp | DB | U | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=reverse+lunge) |
| Cossack Squat | adductors, mobility, lateral stability | Stab/Mob | BW/light | U | ✓ | [🎥](https://www.youtube.com/@DeltaBolic/search?query=cossack+squat) |

## Horizontal push
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Barbell Bench Press | chest, triceps, front delt | Str/Hyp | BB, bench, rack | | ✓ | [🎥](https://www.youtube.com/@DeltaBolic/search?query=bench+press) |
| Incline Bench Press | upper chest, triceps | Str/Hyp | BB, bench | | ✓ | [🎥](https://www.youtube.com/@DeltaBolic/search?query=incline+bench+press) |
| Incline DB Press | upper chest | Hyp/Str | DB, bench | | ✓ | [🎥](https://www.youtube.com/@DeltaBolic/search?query=incline+dumbbell+press) |
| Seated Machine (Incline) Press | chest | Hyp | mach | | ✓ | [🎥](https://www.youtube.com/@DeltaBolic/search?query=machine+chest+press) |
| Dips | lower chest, triceps | Str/Hyp | BW/+weight | | ✓ | [🎥](https://www.youtube.com/@DeltaBolic/search?query=dips) |

## Vertical push
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Overhead Press (BB) | delts, triceps, trunk | Str/Hyp | BB/mini, rack | spine⚠(overhead) | ✓ | [🎥](https://www.youtube.com/@DeltaBolic/search?query=overhead+press) |
| DB Shoulder Press | delts | Hyp/Str | DB | | ✓ | [🎥](https://www.youtube.com/@DeltaBolic/search?query=dumbbell+shoulder+press) |

## Horizontal pull
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Barbell Bent-Over Row | lats, rhomboids, erectors | Str/Hyp | BB | spine⚠ | ✓ | [🎥](https://www.youtube.com/@DeltaBolic/search?query=barbell+row) |
| Seated Cable Row | lats, mid-back | Str/Hyp | cable/mach | | ✓ | [🎥](https://www.youtube.com/@DeltaBolic/search?query=seated+cable+row) |
| Dual Pulley Row | lats, mid-back | Str/Hyp | cable | | ✓ | [🎥](https://www.youtube.com/@DeltaBolic/search?query=dual+pulley+row) |
| Chest-supported Row (machine) | mid-back (no spine load) | Hyp | mach | | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=chest+supported+row) |

## Vertical pull
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Pull-up | lats, biceps | Str/Hyp | BW, bar | | ✓ | [🎥](https://www.youtube.com/@DeltaBolic/search?query=pull+up) |
| Weighted Pull-up | lats, biceps | Str | +weight, bar | | ✓ | [🎥](https://www.youtube.com/@DeltaBolic/search?query=weighted+pull+up) |
| Lat Pulldown | lats | Hyp/Str | cable/mach | | ✓ | [🎥](https://www.youtube.com/@DeltaBolic/search?query=lat+pulldown) |

---

## POWER / explosive — do FIRST, fresh, low reps (1–5), max intent, NOT to failure
Sub-grouped by ProPower pattern. **Transfer is narrow — train the pattern you need** (`ProPower (Power & RFD).md`). Pick a pattern **not** hit recently to broaden the vector.

### Vertical push / triple-extension-up
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Push Press | explosive vertical push (leg drive→overhead) | Pow/Str | BB/DB | skill | ✓ | [🎥](https://www.youtube.com/@DeltaBolic/search?query=push+press) |
| Jump Squat (light) | lower explosive | Pow | BW/light | calf, ecc | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=jump+squat) |
| Box Jump | lower-body explosive + vertical | Pow | box | calf | ✓ | [🎥](https://www.youtube.com/@DeltaBolic/search?query=box+jump) |
| Trap-bar Jump | total-body explosive (loaded) | Pow | trap | calf, skill | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=trap+bar+jump) |

### Hinge / posterior ballistic
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Kettlebell Swing | posterior chain (hip power) | Pow | KB | | ✓ | [🎥](https://www.youtube.com/@DeltaBolic/search?query=kettlebell+swing) |
| Power Clean | total posterior explosive | Pow | BB | skill | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=power+clean) |
| Broad Jump | horizontal hip explosive | Pow | BW | calf, ecc | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=broad+jump) |

### Horizontal push
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Plyo Push-up (clap) | explosive horizontal push | Pow | BW | | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=plyo+push+up) |
| Med-ball Chest Pass | explosive horizontal push | Pow | med, wall | wall | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=medicine+ball+chest+pass) |
| Speed Bench (~50–60%) | RFD on the bench pattern | Pow | BB, bench | | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=speed+bench+press) |

### Horizontal / vertical pull (explosive)
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Barbell High Pull | explosive pull (traps, posterior) | Pow | BB | skill | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=barbell+high+pull) |
| Speed Row (~50–60%) | RFD on the row pattern | Pow | BB/cable | | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=explosive+row) |

### Rotation (no wall needed → cable)
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Explosive Cable Rotation | rotational power (hips→trunk) | Pow | cable | | ✓(rotation) | [🎥](https://www.youtube.com/@DeltaBolic/search?query=explosive+cable+rotation) |
| Cable Chop (fast) | diagonal rotational power | Pow | cable | | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=cable+chop) |
| Med-ball Rotational Throw | rotational power | Pow | med, wall | wall | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=medicine+ball+rotational+throw) |

### Locomotor / reactive (SSC-dominant)
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Pogo Hops | ankle stiffness / reactive | Pow | BW | calf | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=pogo+hops) |
| Bounding | reactive horizontal | Pow | BW | calf, ecc | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=bounding+drill) |
| Skater Bounds | reactive lateral | Pow | BW | calf, ecc | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=skater+bounds) |
| Depth Jump | reactive SSC (advanced) | Pow | box | calf, ecc, skill | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=depth+jump) |

### Landing / deceleration (eccentric power — the neglected one)
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Drop Landing (stick the landing) | eccentric absorb / fall-arrest | Pow | box/BW | calf, ecc | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=drop+landing+drill) |
| Snap-down | rapid deceleration / athletic position | Pow | BW | | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=snap+down+drill) |

### Speed reps (RFD on the main lifts)
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Speed reps (squat/bench/pull ~50–60%) | RFD on a main lift | Pow | BB | | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=speed+squat+dynamic+effort) |

---

## Carries (anti-lateral-flexion / grip / trunk — Core Stability)
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Suitcase Carry | obliques/QL (anti-lat-flex) | Stab/ME | DB/KB | U, calf | ✓ | [🎥](https://www.youtube.com/@DeltaBolic/search?query=suitcase+carry) |
| Farmer Carry | grip, trunk, total | Stab/ME | DB/KB/trap | calf | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=farmer+carry) |
| Front-rack Carry | anti-extension, trunk | Stab | KB/DB | calf | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=front+rack+carry) |
| Overhead Carry | shoulder stab, anti-extension | Stab | KB/DB | calf | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=overhead+carry) |
| Bottom-up KB Carry | grip + shoulder stability | Stab | KB | U | ✓ | [🎥](https://www.youtube.com/@DeltaBolic/search?query=bottoms+up+kettlebell+carry) |

## Core / anti-rotation / stability (Core Stability model)
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| McGill Curl-up | anti-extension (anterior core) | Stab | BW | | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=mcgill+curl+up) |
| Side Plank | anti-lateral-flexion (QL/obliques) | Stab | BW | | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=side+plank) |
| Bird Dog | anti-rotation, spinal control | Stab | BW | | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=bird+dog) |
| Pallof Press | anti-rotation | Stab | cable/band | | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=pallof+press) |
| Dead Bug | anti-extension, coordination | Stab | BW | | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=dead+bug) |
| Standing Cable Rotation | rotation control | Stab/Hyp | cable | | ✓ | [🎥](https://www.youtube.com/@DeltaBolic/search?query=standing+cable+rotation) |
| Decline Crunch | rectus (dynamic flexion) | Hyp/ME | bench/+plate | spine⚠(flexion) | ✓ | [🎥](https://www.youtube.com/@DeltaBolic/search?query=decline+crunch) |
| Russian Twist | obliques (rotation) | Hyp/ME | bench/+plate | spine⚠(flexion) | ✓ | [🎥](https://www.youtube.com/@DeltaBolic/search?query=russian+twist) |

## Calf / lower-leg (rehab + tolerance)
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Single-leg Heel Raise (Alfredson, eccentric) | gastroc/soleus + Achilles | Rehab/Str | BW/step | U, calf | ✓ | [🎥](https://www.youtube.com/@DeltaBolic/search?query=alfredson+heel+drop) |
| Standing Calf Raise | gastrocnemius (knee straight) | Hyp | mach/DB | calf | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=standing+calf+raise) |
| Seated Calf Raise | soleus (knee bent) | Hyp | mach | calf | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=seated+calf+raise) |

## Isolation patches (weak-link fillers)
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Lateral Raises | side delts | Hyp | DB/cable | | ✓ | [🎥](https://www.youtube.com/@DeltaBolic/search?query=lateral+raises) |
| Face Pulls | rear delts, shoulder health | Hyp/Stab | cable/band | | ✓ | [🎥](https://www.youtube.com/@DeltaBolic/search?query=face+pulls) |
| Biceps Curl | biceps | Hyp | DB/BB/mini | | ✓ | [🎥](https://www.youtube.com/@DeltaBolic/search?query=biceps+curl) |
| Triceps Pushdown | triceps | Hyp | cable | | ✓ | [🎥](https://www.youtube.com/@DeltaBolic/search?query=triceps+pushdown) |

## Mobility / activation (warm-up; Cook readiness)
| Exercise | Primary | Adapt | Equip | Flags | Fam | 🎥 |
|---|---|---|---|---|---|---|
| Couch Stretch (hip flexor) | hip flexors (unblock glute) | Mob | BW | | | [🎥](https://www.youtube.com/@DeltaBolic/search?query=couch+stretch) |
| Hip 90/90 | hip rotation mobility | Mob | BW | | ✓ | [🎥](https://www.youtube.com/@DeltaBolic/search?query=hip+90+90) |

> **Glute activation priming** (Banded Glute Bridge, Clamshell, Lateral Band Walk) lives in **Hip extension / glute** above — use those rows rather than duplicating them here.
