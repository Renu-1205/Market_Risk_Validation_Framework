# Market Risk Validation Framework

## Overview

This project is a Python-based implementation of a Market Risk Validation Framework for a multi-asset portfolio. It applies standard quantitative risk techniques used in financial institutions to measure, compare, and validate portfolio downside risk.

The framework integrates Historical VaR, Parametric VaR, Monte Carlo simulation, Expected Shortfall, backtesting, correlation analysis, and stress testing to evaluate both risk magnitude and model reliability.

---

## Objective

* Estimate portfolio risk using multiple VaR methodologies
* Compare empirical vs model-based risk estimates
* Validate VaR performance using statistical backtesting
* Assess tail risk through Expected Shortfall
* Evaluate portfolio behavior under stress scenarios

---

## Dataset

* Source: Yahoo Finance (via `yfinance`)
* Assets:

  * HDFC Bank
  * Reliance
  * TCS
  * NIFTYBEES ETF
  * GOLDBEES ETF
* Period: ~2020–2025 daily price data

---

## Methodology

### 1. Data Processing

* Downloaded historical price data
* Handled missing values
* Computed daily percentage returns
* Constructed weighted portfolio returns

### 2. Risk Estimation Models

* Historical VaR (empirical quantile method)
* Parametric VaR (mean-variance normal assumption)
* Monte Carlo VaR (multivariate normal simulation)

### 3. Tail Risk Measure

* Expected Shortfall (conditional loss beyond VaR)

### 4. Model Validation

* VaR backtesting using breach frequency
* Kupiec Proportion of Failures test

### 5. Risk Structure Analysis

* Correlation matrix for diversification assessment

### 6. Stress Testing

* Scenario-based shocks:

  * Equity market crash
  * Interest rate shock
  * Flight-to-safety regime
  * Mild correction scenario

---

## Key Outputs

* Portfolio VaR estimates across three methods
* Expected Shortfall for tail-risk severity
* Statistical validation of VaR model (Kupiec test)
* Stress scenario loss estimates
* Correlation-driven diversification insights

---

## Key Insight

Historical VaR is more conservative than model-based VaR methods, indicating the presence of fat tails and extreme market events not fully captured by normal distribution assumptions.

---

## Tools & Libraries

* Python
* Pandas
* NumPy
* Matplotlib
* SciPy
* yfinance

---

## Conclusion

This project demonstrates an end-to-end implementation of institutional-style market risk measurement and validation techniques, bridging statistical modeling with financial risk management applications.

---

## Author

Economics postgraduate with focus on quantitative finance, econometrics, and risk analytics.
