# Portfolio Optimization with Monte Carlo Simulation

A theory-backed walkthrough of multi-asset portfolio construction, optimization, and risk analysis, built on a 7-asset universe (AAPL, JPM, PG, NFLX, SPTL, VCLT, GC=F) spanning equities, bonds, and gold.

The notebook combines classical portfolio theory with modern risk-simulation techniques to construct, compare, and stress-test three risk-profile portfolios (Aggressive / Moderate / Conservative).

## What's inside

1. **Data & Returns** — log returns, why they're used over simple returns, live data via `yfinance` with a synthetic correlated-price fallback
2. **Risk-Profile Portfolios** — hand-built Aggressive / Moderate / Conservative baselines
3. **Markowitz Mean-Variance Optimization** — classical MPT (1952)
4. **Beyond Markowitz** — Risk Parity (Equal Risk Contribution) and other techniques addressing MVO's sensitivity to estimation error
5. **Efficient Frontier** — visualized against 15,000 random portfolios, with per-asset risk contribution breakdown
6. **Monte Carlo Simulation (3 engines)** — Cholesky (Gaussian), Student-t (fat tails), and Bootstrap (historical resampling), 8,000 simulations each
7. **Risk Metrics** — VaR, CVaR, and related tail-risk quantification
8. **1-Year Simulated Outlook** — comparison across all three portfolios and all three MC engines, with fan charts
9. **Scenario Analysis** — portfolio behavior across Bull/Neutral/Bear market regimes
10. **Stress Testing** — historical crisis replays plus hypothetical shocks
11. **Summary & Takeaways**

## Methods

- Markowitz mean-variance optimization (`scipy.optimize.minimize`)
- Risk Parity / Equal Risk Contribution
- Monte Carlo simulation: Cholesky decomposition, Student-t, historical bootstrap
- Value-at-Risk (VaR) and Conditional VaR (CVaR)
- Historical and hypothetical stress testing

## Setup

```bash
pip install -r requirements.txt
jupyter notebook Portfolio_Optimization_Monte_Carlo.ipynb
```

Data loads live via `yfinance`; if network/data access fails, the notebook automatically falls back to a synthetic but realistically-correlated price series, so it runs end-to-end either way.

## Tech stack

`numpy` · `pandas` · `scipy` · `matplotlib` · `seaborn` · `yfinance`

## Author

Yuvraj Singh
