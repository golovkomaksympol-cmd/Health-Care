# Onco Screening

The "Rabbit Hunt" strategy. Hunt the diseases that actually kill people in the patient's age band; ignore the ones that generate noise without survival benefit.

## Universal (any sex)

| Procedure | Target | Frequency | Notes |
|:---|:---|:---|:---|
| **Colonoscopy + Gastroscopy** (bidirectional endoscopy under sedation) | Colorectal cancer + gastric cancer + mucosal evaluation | Colonoscopy: every 5-10 years starting age 45 (40 if family history). Gastroscopy: by symptoms / iron malabsorption workup | Combine in one sedation session when possible |
| **Skin / mole mapping** (FotoFinder or equivalent) | Melanoma | Annually | Critical for fair-skinned patients and anyone with >50 moles or atypical nevi |
| **CT Angiogram → CAC score** | Atherosclerotic CV disease (technically not cancer, but tail-risk hedging) | Once at 40-50, repeat if elevated | Triggered by elevated ApoB or Lp(a); see `Trigger Diagnostics.md` |

## Female-specific

| Procedure | Target | Frequency | Notes |
|:---|:---|:---|:---|
| **Mammography** / **Breast MRI** | Breast cancer | Annually starting age 40 | MRI preferred if dense breast tissue or BRCA risk |
| **Breast ultrasound** | Breast cancer adjunct | Annually (alternate with mammography) | Useful for dense tissue between mammograms |
| **Pap test + HPV** | Cervical cancer | Every 3-5 years if HPV negative | After 3 normal results, can extend interval |
| **Transvaginal pelvic ultrasound** | Ovarian / uterine status | Annually | If suspicious mass (complex cyst with blood flow) → **CA-125 + HE4** (ROMA index) to route: gynecologist vs gyne-oncologist |

## Male-specific

| Procedure | Target | Frequency | Notes |
|:---|:---|:---|:---|
| **PSA + free PSA ratio** | Prostate cancer | Annually starting age 45 (40 if family history) | Use trends and free/total ratio, not single absolute |
| **Testicular self-exam** | Testicular cancer | Monthly | Highest yield for men 20-40; high-curability if caught early |
| **Multiparametric prostate MRI** | Prostate cancer (high-risk patients) | Triggered by elevated/rising PSA | Avoid unnecessary biopsy |

## Lab markers (blood / stool)

| Marker | Target | Optimum | Note |
|:---|:---|:---|:---|
| **Helicobacter Pylori** (stool antigen) | Stomach | Negative | If positive → eradication course (reduces gastric cancer risk by ~80%) |
| **FIT (fecal immunochemical test)** | Colorectal | Negative | Annual, as a between-colonoscopy interim screen |

## ❌ Black list — do NOT order without symptoms

| Test | Why not |
|:---|:---|
| **CA-19-9, CA-15-3, CEA** | High false-positive rate in asymptomatic patients. Lots of noise, no survival benefit. |
| **Whole-body PET-CT** | Excess radiation, lots of incidental findings, no proven mortality benefit as screening. |
| **AFP** (without cirrhosis / hepatitis history) | False-alarm generator (Gigerenzer principle). |
| **17-OH Progesterone** in adults without childhood symptoms | If they had congenital adrenal hyperplasia, it would have presented in childhood. Adult-onset hits ~zero base rate. |
| **ApoA1** | Tactics are driven by absolute ApoB; ApoA1 doesn't change the protocol in any scenario. |
| **"Comprehensive tumor marker panel"** (anything sold as a single-tube cancer screen) | Predictive value approaches zero in unselected asymptomatic patients. |

## Decision rule for screening

A test passes the screening filter only if:

1. The disease is **prevalent enough** in this patient's bucket (age, sex, family history) to justify the workup.
2. There's a **treatable window** if caught early (vs late).
3. **Sensitivity and specificity are good enough** that a positive moves the action plan, and a negative is reliably reassuring.
4. The downstream of a positive isn't worse than the disease (the over-treatment trap).

Anything that fails (1) is fishing. Anything that fails (3) is anxiety generator. Anything that fails (4) is iatrogenic harm.
