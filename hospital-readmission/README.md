# Hospital Readmission Risk — Classification

**Problem:** predict which patients are at risk of readmission within 30 days of discharge, so staff can target follow-up care and reduce financial penalties.

**Approach:** a **Gradient Boosting Classifier** on EHR-style features (time in hospital, number of medications, lab procedures, diagnoses). Evaluated with a full classification report, focusing on the **readmit class**.

**Result (simulated data):** readmit-class precision 0.57, recall 0.51, F1 0.54 (vs 0.90 F1 for the discharged-safely class) — a realistic reflection of how hard the minority, high-stakes class is.

**Key insight:** in clinical triage, **recall on the readmit class** matters more than overall accuracy — missing a high-risk patient is the costly error.

> Data is generated in-notebook (simulated). Run `hospital_readmission_risk.ipynb`.
