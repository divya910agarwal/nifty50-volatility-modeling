# Volatility Modeling and Forecasting — Nifty50

Empirical analysis of Nifty50 daily returns (1995–2024) using GARCH-family models.

## Methodology
- **Data:** 7,151 daily observations, Nov 1995 – Aug 2024
- **Preprocessing:** Log returns, stationarity (ADF), ARCH-LM test to justify model selection
- **Models:** GARCH(1,1), EGARCH(1,1), GJR-GARCH(1,1), APARCH(1,1)
- **Evaluation:** In-sample via AIC/BIC, out-of-sample via MSE/MAE (90/10 split, expanding window)

## Key Findings
- GJR-GARCH superior in-sample (AIC: 23007.9, BIC: 23042.3)
- APARCH superior out-of-sample (MSE: 4.343, MAE: 0.941)
- Leverage effect confirmed: negative shocks increase volatility ~2.4x more than positive shocks (γ = 0.091, p < 0.001)
- Nifty50 returns exhibit fat tails (kurtosis: 12.12), negative skewness, and strong volatility clustering

## Tools
Python — `arch`, `statsmodels`, `pandas`, `numpy`, `matplotlib`
