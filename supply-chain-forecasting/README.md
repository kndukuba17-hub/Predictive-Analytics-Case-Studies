# Supply-Chain Demand Forecasting — Time Series

**Problem:** forecast daily product demand so procurement teams avoid both stockouts (lost sales) and overstock (tied-up capital).

**Approach:** a **Gradient Boosting Regressor** on engineered time features — **autoregressive lag features** (e.g. sales 7 days ago), **rolling averages**, and date parts (day-of-week, month). Critically, the model uses a **strict sequential train/test split** (train on the earlier period, test on a held-out future window) — time-ordered data must never be randomly shuffled.

**Result (simulated data):** MAE ~43 units/day, R² 0.13 — deliberately noisy synthetic demand makes this a harder, more honest forecasting target.

**Key insight:** correct time-series methodology (sequential split, lag/rolling features) is the point here, not a headline accuracy number.

> Data is generated in-notebook (simulated). Run `retail_demand_forecasting.ipynb`.
