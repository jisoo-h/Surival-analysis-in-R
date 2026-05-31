# Surival-analysis-in-R
Survival analysis in R project to demonstrate a broad range of time-to-event methods using the NCCTG Lung Cancer dataset (lung) bundled with R's {survival} package

# Survival Analysis in R

A self-contained project demonstrating a broad range of time-to-event methods using the NCCTG Lung Cancer dataset (`lung`) bundled with R's `{survival}` package — no external downloads required.

---

## Dataset: `lung`

228 patients with advanced lung cancer from the North Central Cancer Treatment Group.

| Variable | Description |
|---|---|
| `time` | Survival time (days) |
| `status` | 1 = censored, 2 = dead |
| `sex` | 1 = Male, 2 = Female |
| `age` | Age in years |
| `ph.ecog` | ECOG performance score (0–4) |
| `ph.karno` | Karnofsky score rated by physician |
| `pat.karno` | Karnofsky score rated by patient |
| `meal.cal` | Calories at meals |
| `wt.loss` | Weight loss in last 6 months (lbs) |

---

## Setup

Install required packages (one-time):

```r
install.packages(c(
  "survival", "survminer", "flexsurv",
  "cmprsk", "survcomp", "pec", "timeROC",
  "ggplot2", "dplyr", "tidyr"
))
```

---

## Scripts

### `R/analysis.R` — Core survival analysis

| What it does | Output |
|---|---|
| Kaplan-Meier curves: overall, by sex, by ECOG | `km_by_sex.png`, `km_by_ecog.png` |
| Log-rank tests | Console |
| Cox PH model + forest plot | `cox_forest.png` |
| Schoenfeld residuals (PH assumption) | `schoenfeld_residuals.png` |
| Predicted survival for patient profiles | `predicted_survival.png` |

```r
setwd("survival_analysis")
source("R/analysis.R")
```

