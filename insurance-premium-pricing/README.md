# Insurance Premium Pricing — Regression

**Problem:** predict an individual's medical costs (the basis of actuarial pricing) from demographic and lifestyle risk factors. Underprice and the insurer loses money; overprice and they lose customers.

**Approach:** a **Random Forest Regressor** on features including age, BMI, smoking status and dependents, evaluated with R², MAE and RMSE. Feature importances expose the dominant cost drivers.

**Result (simulated data):** R² 0.98, MAE ~£1,352, RMSE ~£1,713. The high R² reflects the clean synthetic relationships — a real dataset would be noisier.

**Key insight:** the model captures the **non-linear compound risk of smoking combined with high BMI**, which a simple linear model would understate.

> Data is generated in-notebook (simulated). Run `insurance_premium_pricing.ipynb`.
