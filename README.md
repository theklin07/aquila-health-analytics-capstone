# Aquila Health Network — Enterprise Business Analytics Capstone

**Optimizing Clinical Operations Through Enterprise Business Analytics at Aquila Health Network**
NYU MS in Management & Systems — MASY GC-4100 Applied Project Capstone (Spring 2026)
Karen Lin · Sponsor: Dan Stone, Damark Group, Inc.

> Aquila Health Network is a fictional 40-clinic outpatient system built for this capstone. All data is
> synthetic (~5,000 generated appointment records, scaled to a realistic 40-clinic / 200-provider
> network) — no real patient, provider, or clinic data is used anywhere in this repo.

An interactive write-up of these findings is here: **[Aquila Ledger](https://claude.ai/artifact/S8Mohe88NY44fUUEtCSJuz)**

## What this project does

Aquila's leadership had no unified view of clinical operations — no-shows, provider utilization,
referral follow-through, and patient wait times were all invisible across the network. This project
builds a centralized analytics platform to close that gap:

1. **Requirements** — a sponsor-approved Functional Requirements Specification defining KPIs, data
   requirements, and dashboard scope.
2. **Data modeling** — a star-schema data mart (`FactAppointment` + five dimension tables) and a
   5,000-row synthetic dataset generated to match it.
3. **Dashboards** — five interactive Tableau dashboards: Clinical Operations, Revenue & Access,
   Provider Utilization, Referral Performance, and No-Show Risk.
4. **Predictive model** — a logistic regression proof-of-concept scoring appointments by no-show
   probability (ROC-AUC 0.595), with documented assumptions and feature importance.
5. **Delivery** — a final written report and sponsor presentation synthesizing findings and
   recommendations.

## Key results

| Metric | Value |
|---|---|
| Appointments modeled | 5,000 across 40 clinics / 200 providers |
| Network no-show rate | 18.1% (vs. a 15%-reduction sponsor target) |
| Average patient wait | 23.79 days (vs. a 19-day FRS target) |
| Provider utilization | 51.3%–58.6% across all 8 specialties (target: 82%) |
| Incomplete referrals | 384 of 1,500 (26%) — pending or never scheduled |
| Predictive model | Logistic regression, ROC-AUC 0.595, recall 0.49 on no-shows |

Full findings, recommendations, and the click-through explanation of every chart are in the
[interactive case study](https://claude.ai/artifact/S8Mohe88NY44fUUEtCSJuz).

## Repo structure

```
aquila-health-analytics-capstone/
├── README.md
├── data/
│   └── Aquila_Synthetic_Dataset.xlsx        # 6-table star-schema dataset (~5,000 appointments)
├── notebooks/
│   └── Aquila_NoShow_Predictive_Model.ipynb  # logistic regression model, Python / scikit-learn
├── dashboards/
│   └── Aquila_Capstone.twb                   # Tableau workbook (5 dashboards)
├── presentation/
│   └── Aquila_Capstone_Presentation.pdf       # final sponsor presentation
└── docs/
    ├── Project_Charter.docx
    ├── Functional_Requirements_Specification.docx
    ├── Project_Status_Report.pdf
    ├── Annotated_Bibliography.docx
    ├── Literature_Review.docx
    └── WBS_Gantt.xlsx
```

## Tech stack

- **Data modeling & generation:** star-schema dimensional design, Python (pandas)
- **Dashboards:** Tableau Public — [live dashboards →](#) <!-- add published Tableau Public URL -->
- **Predictive analytics:** Python, scikit-learn (`LogisticRegression`, balanced class weighting)
- **Methodology:** CRISP-DM (business understanding → data understanding → data preparation →
  modeling → evaluation)

Tableau was substituted for Power BI mid-project (Power BI Desktop is Windows-only; development was
on a MacBook) — approved by the project sponsor and documented in the Project Status Report.

## Limitations

This is an academic proof-of-concept, not a production system: the dataset is synthetic, the
predictive model is a logistic-regression baseline (a Random Forest or XGBoost model would likely
improve on its 0.595 ROC-AUC), and no live EHR integration exists. See `docs/Project_Charter.docx`
for full scope and constraints.

## Author

**Karen Lin** — [portfolio](#) <!-- add portfolio URL --> · kn97na@gmail.com
