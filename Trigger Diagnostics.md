# Trigger Diagnostics

Stage-2 diagnostics. These tests are **not ordered by default**. They're triggered by a specific finding from the baseline panel — if-then rules below.

The point: every additional test should change an action. If the result wouldn't change the plan, the test is anxiety, not information.

## How to use this file

1. Run the **baseline panel** first (see `Decision Principles.md` → signal-to-noise; the panel itself is assembled by the `lab-panel` skill).
2. Read the baseline against the triggers below.
3. Order a stage-2 test **only** when its trigger fired **and** you can name the action each possible result would produce.

**The gatekeeper question — ask it out loud for every candidate test:**
> "If this comes back high, what do I do? If it comes back normal, what do I do?"
> Same answer to both → **don't order it.**

**Two standing rules:**
- **Cheap sentinel before expensive confirmer.** Order the widely-available marker that gates the rare diagnosis, not the rare marker itself. A normal sentinel closes the question at a fraction of the cost/friction.
- **A trigger is not a diagnosis.** It routes you to the next test, nothing more.

## Cardiometabolic

| Trigger (baseline finding) | Then order | Why — what action it changes |
|:---|:---|:---|
| **ApoB above target** on current therapy | Adherence check **first**, then lipid panel + ApoB after 6–8 wk | Distinguishes "dose too low" from "not taken". Escalating a drug that isn't being swallowed fixes nothing |
| **ApoB high** OR **Lp(a) elevated** | **CT Angiogram / CAC score** | A CAC > 0 converts a statistical argument into an anatomical one — moves a hesitant patient (and doctor) to treat |
| **Statin started / dose escalated** | **CK** (+ ALT/AST) | Safety baseline for myopathy. Muscle pain *without* CK elevation is usually not the drug — prevents stopping an effective therapy for the wrong reason |
| **Fasting glucose / HbA1c borderline** | Fasting **insulin → HOMA-IR** | Detects compensated insulin resistance years before glucose drifts. Glucose alone is the last thing to break |
| **HOMA-IR borderline and moving** | **HbA1c** as the low-noise anchor | HOMA-IR is a high-variance marker; HbA1c integrates ~3 months and won't flip on one noisy draw |
| **Triglycerides high + HDL low** | TG/HDL ratio, TyG index (both **calculated**, no new blood) | Free insulin-resistance signal from data already in hand |

## Iron, blood, and the HbA1c confounder

| Trigger | Then order | Why |
|:---|:---|:---|
| **Ferritin low** + low MCV/MCH | Serum iron + **TIBC/transferrin + TSAT**, B12, folate | Separates iron-deficiency from B12/folate anemia — different treatments |
| **Ferritin low-normal but symptomatic** | **CRP/hsCRP alongside** | Ferritin is an **acute-phase reactant** — inflammation inflates it and can mask real depletion. Never read ferritin without an inflammation marker |
| **Iron deficiency present AND HbA1c being used for glycemic decisions** | Interpret HbA1c **only** together with ferritin | Iron deficiency **falsely raises** HbA1c. Correcting iron lowers HbA1c independently of glycemia — don't credit that drop to diet |
| **Ferritin not rising** after 3 months of adequate supplementation | Reassess absorption: coeliac serology, **H. pylori**, consider gastroscopy; confirm dosing/timing | Malabsorption vs non-adherence vs ongoing loss — three different fixes |
| **Low platelets** (or falling trend) | **B12 + folate first**; if normal → haematology referral | B12/folate deficiency causes thrombocytopenia *and* raised homocysteine — one cheap cause explaining two findings. Only then chase MDS/ITP/hypersplenism |
| **Homocysteine elevated** | **B12 + folate** (before any B-complex) | Identifies which substrate is missing. Supplementing blind removes the diagnostic signal |
| **Any unexplained anemia in an adult** | Faecal occult blood / endoscopy per age & risk | Occult GI blood loss is the diagnosis you cannot afford to miss |

## Bone, calcium, vitamin D

| Trigger | Then order | Why |
|:---|:---|:---|
| **Loading vitamin D at high dose for months** | **Total calcium** (with albumin correction) | Cheap safety sentinel for creeping hypercalcemia |
| **Calcium high or pressing the upper limit** | **PTH (intact)** ± ionised calcium | High Ca + inappropriately normal/high PTH = primary hyperparathyroidism. **Normal calcium closes this question — PTH is then unnecessary** |
| **25(OH)D refractory** (<40 after 3 months of adequate dosing) | **PTH + magnesium** | Distinguishes secondary hyperparathyroidism / Mg-dependent activation failure / malabsorption |
| **Osteopenia or osteoporosis on DXA** | Calcium, 25(OH)D, PTH, TSH; consider coeliac | Rules out treatable secondary causes before committing to long-term therapy |

## Thyroid

| Trigger | Then order | Why |
|:---|:---|:---|
| **TSH outside target** | **fT4** (+ fT3 if conversion is the question) | TSH alone can't separate central from peripheral problems |
| **Abnormal thyroid + goitre/nodules** | **Anti-TPO** (once) + ultrasound | Establishes autoimmune vs non-autoimmune. Anti-TPO is **inert** — do not re-test on a 3-month cadence expecting movement |
| **fT3 low with adequate fT4** | **Ferritin, selenium status, reverse T3 if justified** | Deiodinase conversion is iron- and selenium-dependent; fix the substrate before adding hormone |
| **Hypothyroid symptoms, normal TSH/fT4** | Stop. Re-derive the question | This is where low-value testing breeds. Absent a real trigger, more thyroid panels generate noise |

## Sex hormones / HRT gate

| Trigger | Then order | Why |
|:---|:---|:---|
| **Irregular cycles + endometrial thickening** | Pelvic ultrasound; progestagen challenge per gynaecology | Unopposed estrogen drives hyperplasia risk — the action is cyclical progestagen, not more bloods |
| **FSH high + estradiol low + symptoms** | Confirm menopausal status; then the HRT contraindication workup | Gates the whole HRT decision |
| **HRT being considered + history of pregnancy loss / thrombosis** | **Thrombophilia panel** (Protein S/C, Factor V Leiden, antiphospholipid, prothrombin G20210A) | A positive result changes the *route*: transdermal estrogen rather than oral |
| **Irregular cycle** | **Do NOT order luteal progesterone** | The draw can't be timed to the luteal phase → the result is noise, not signal |

## When NOT to escalate

- **The value sits inside the noise band.** Establish the reference change value before declaring a trend. Repeat the same test under controlled conditions instead of adding new ones.
- **The result wouldn't change management** — the gatekeeper question failed.
- **An acute confounder is active** — infection, recent bleeding, hard training (CK), non-fasting, acute illness. Fix the timing, don't add tests.
- **Tumour markers in asymptomatic screening** (CA-19-9, CA-15-3, CEA, AFP without liver disease) — poor specificity, high false-alarm cost. See `Onco Screening.md` black list.
- **The finding is an imaging incidentaloma with normal biochemistry.** Treat biochemistry + symptoms, not an operator-dependent ultrasound adjective.

> Related: `Models/Iron Homeostasis.md`, `Models/Homocysteine and Methylation.md`, `Models/ApoB and Atherosclerosis.md`, `Models/Mevalonate Pathway.md`, `Models/NNT (Number Needed to Treat).md`, `Onco Screening.md`, `Decision Principles.md`.
