# Aquila Health Network — Business Analytics Capstone

**Course:** MASY GC-4100 Applied Project Capstone, NYU  
**Student:** Karen Lin  
**Sponsor:** Dan Stone, Damark Group Inc.  
**Project Period:** February 9 – May 5, 2026  

---

## Project Overview

This capstone delivers a centralized business analytics platform for Aquila Health Network, a multi-state outpatient healthcare provider operating 40 clinics across the Northeast. The platform enables leadership to monitor clinical operations, optimize appointment utilization, and proactively manage patient access risk.

---

## Repository Contents

| File | Description |
|------|-------------|
| `Aquila_Synthetic_Dataset.xlsx` | Star schema data mart with 5 tables representing clinical operations data |
| `Aquila_Capstone.twbx` | Tableau workbook containing 5 interactive dashboards |
| `Aquila_NoShow_Predictive_Model.ipynb` | Jupyter notebook — logistic regression no-show risk model |

---

## Dashboards (Tableau)

1. **Clinical Operations Dashboard** — Network KPIs, appointment status, heat map by day/hour
2. **Revenue & Access Dashboard** — Revenue by specialty, wait time by clinic, no-show by specialty
3. **Provider Utilization Dashboard** — Utilization vs 82% target by provider and specialty
4. **Referral Performance Dashboard** — Referral status and completion by specialty
5. **No-Show Risk Dashboard** — Risk score distribution and ranked appointment list

---

## Predictive Model

- **Algorithm:** Logistic Regression (balanced class weighting)
- **Target:** Appointment no-show (binary classification)
- **ROC-AUC:** 0.595
- **Top Predictor:** Prior no-show history (coefficient 0.25)
- **Key Finding:** Friday appointments have the highest no-show rate (20.9%); Wednesday the lowest (15.8%)

---

## Key Findings

- Network no-show rate: **18.1%** — exceeds the 15% reduction target threshold
- All specialties below **82% provider utilization target**
- Average patient wait time: **23.79 days** across all clinics
- Paterson Community Clinic has the longest average wait at **26.15 days**
- Primary Care has the highest no-show rate by specialty at **19.0%**
