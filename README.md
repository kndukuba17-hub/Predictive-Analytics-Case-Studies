# Predictive Analytics — Case Studies

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![scikit-learn](https://img.shields.io/badge/scikit--learn-RF%20%7C%20GBM-orange)
![Data](https://img.shields.io/badge/Data-Simulated%20(technique%20demos)-lightgrey)

Three compact, technique-focused predictive-analytics studies across **regression, classification, and time-series forecasting** — each framed around a real business problem.

> **Honest note on data:** these three studies run on **simulated datasets** generated in-notebook. They're here to demonstrate *modelling technique and business framing* across problem types, not to showcase real-data cleaning (see my [CLV](https://github.com/kndukuba17-hub/predictive-clv-engine), [Churn](https://github.com/kndukuba17-hub/Customer-Churn-Prediction) and [Recommender](https://github.com/kndukuba17-hub/B2C-Retail-Analytics-E-Commerce-Recommendation-Engine) projects for that). Metrics below are on simulated data and are illustrative. This repo consolidates three previously separate small projects into one tidy collection.

---

## Contents

| # | Case study | Problem type | Model | Result (simulated data) |
|---|-----------|-------------|-------|------------------------|
| 1 | [Insurance Premium Pricing](insurance-premium-pricing/) | Regression | Random Forest Regressor | R² 0.98*, MAE ~£1,352 |
| 2 | [Hospital Readmission Risk](hospital-readmission/) | Classification | Gradient Boosting | Readmit-class F1 0.54, recall 0.51 |
| 3 | [Supply-Chain Demand Forecasting](supply-chain-forecasting/) | Time series | Gradient Boosting + lag features | MAE ~43 units/day |

<sub>*The 0.98 R² reflects clean synthetic relationships — a real actuarial dataset would be noisier. Stated openly.</sub>

---

### Insurance Premium Pricing (regression)
Predicting individual medical costs from age, BMI, smoking status and dependents — the core of actuarial pricing. Demonstrates regression modelling and the non-linear compound effect of smoking × high BMI. → [details](insurance-premium-pricing/)

### Hospital Readmission Risk (classification)
Flagging patients at risk of 30-day readmission from EHR-style features, to support discharge triage. Demonstrates classification with an emphasis on the readmit-class recall/precision trade-off. → [details](hospital-readmission/)

### Supply-Chain Demand Forecasting (time series)
Forecasting daily product demand using **lag features, rolling windows, and a strict sequential train/test split** (no random shuffling of time-ordered data). → [details](supply-chain-forecasting/)

---

## Tech Stack
Python · pandas · NumPy · scikit-learn (Random Forest, Gradient Boosting) · Matplotlib · Seaborn

## How to Run
```bash
git clone https://github.com/kndukuba17-hub/Predictive-Analytics-Case-Studies.git
cd Predictive-Analytics-Case-Studies
pip install -r requirements.txt
jupyter notebook   # open any case-study folder's notebook
```
Each notebook generates its own simulated data — no external download required.
