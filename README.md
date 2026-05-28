# MLE Estimation in Linear Regression

> **CIE 457 — Statistical Inference and Data Analysis**  
> University of Science and Technology, Zewail City · Spring 2026

---

## Overview

This project builds a rigorous understanding of **Maximum Likelihood Estimation (MLE)** applied to linear regression — from first-principles derivation all the way to simulation and real data analysis.

The focus is not just fitting a model, but understanding **how the estimator behaves as a random variable** under different noise assumptions.

---

## Topics Covered

| Section | Description |
|---------|-------------|
| **3.1 — Theory** | Likelihood function derivation, OLS and WLS from MLE, model assumptions |
| **3.2 — Homoscedastic Noise** | OLS estimator distribution via Monte Carlo simulation, comparison to theoretical distribution |
| **3.3 — Heteroscedastic Noise** | OLS vs WLS comparison, effect of noise misspecification on estimator efficiency |
| **3.4 — Inference** | Confidence intervals and prediction intervals, interpretation and comparison |
| **3.5 — Real Data** | Applied regression on a real dataset, residual analysis, heteroscedasticity evidence |
| **Bonus — Fisher Information & CRLB** | Cramér-Rao Lower Bound derivation, proof that OLS achieves the CRLB, sufficient statistics via Factorization Theorem |

---

## Key Results

- Implemented **OLS** `(X'X)^{-1} X'y` and **WLS** `(X'Σ⁻¹X)^{-1} X'Σ⁻¹y` from scratch using NumPy (no sklearn)
- Ran **5000-iteration Monte Carlo simulations** to empirically characterize estimator distributions and confirmed they match the theoretical Gaussian `β̂ ~ N(β, σ²(X'X)⁻¹)`
- Showed that **WLS is more efficient than OLS** under heteroscedastic noise by comparing covariance trace
- Verified that **OLS achieves the Cramér-Rao Lower Bound** — it is the minimum variance unbiased estimator (MVUE)
- Applied the **Factorization Theorem** to identify sufficient statistics `T₁ = X'y` and `T₂ = y'y`, demonstrating lossless data compression from n observations to 3 numbers

---

## Tech Stack

- **Python 3**
- **NumPy** — matrix operations, OLS/WLS implementation
- **SciPy** — KDE, statistical distributions
- **Matplotlib** — all visualizations

---

## File Structure

```
├── MLE_Estimation_in_Linear_Regression_Project.ipynb   # Full code + outputs
└── README.md
```

[📄 View Report](./MLE Estimation in Linear Regression Project Report.pdf)
---



## Authors

- **Ahmed Gamal** — [@AhmedGamal04](https://github.com/AhmedGamal04)
- **Khaled Mahmoud**
