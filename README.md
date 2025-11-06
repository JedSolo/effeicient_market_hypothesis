# TESTING THE LIMITS OF THE EFFICIENT MARKET HYPOTHESIS: EVIDENCE FROM EQUITY AND CRYPTOCURRENCY MARKETS

This project investigates the robustness of the **Efficient Market
Hypothesis (EMH)** across two contrasting asset classes:

-   **S&P 500 Index (SPX)** --- mature, highly liquid equity market
-   **Bitcoin (BTC-USD)** --- emerging, sentiment-driven cryptocurrency
    market

By combining traditional econometric models with modern machine learning
techniques, the study examines whether daily returns exhibit random walk
behaviour (supporting EMH) or reveal predictable structures inconsistent
with market efficiency.

## Research Questions

1.  Do daily returns of SPX and BTC follow a random walk, or do they
    show predictable patterns?
2.  Can machine learning models (e.g., XGBoost) outperform econometric
    baselines such as ARIMA and GARCH?
3.  Do predictive patterns translate into meaningful economic value when
    backtested?
4.  How does market efficiency differ between a mature equity market and
    an emerging cryptocurrency market across different regimes (bull,
    bear, stagnant)?

## Methodology Overview

The project follows a structured empirical workflow:

### 1. Data Collection & Preprocessing

-   Daily SPX and BTC prices (2015--2024) via **Yahoo Finance**
    (`yfinance`).
-   Transformation and cleaning:
    -   Log returns computation
    -   Forward-fill for missing values
    -   Date alignment across markets
    -   Stationarity testing (ADF)
-   Descriptive statistics and preliminary diagnostics

### 2. Econometric Modeling

#### ARIMA (1,0,1)

-   Tests for linear autocorrelation and weak-form EMH.
-   Residual diagnostics via Ljung--Box Q-test.

#### GARCH (1,1)

-   Captures volatility clustering and conditional heteroskedasticity.
-   Interprets α (shock impact), β (volatility persistence), and α+β
    (long memory).

### 3. Machine Learning Modeling

#### XGBoost Regression

-   Captures nonlinear patterns and higher-order interactions.
-   Includes features such as lagged returns, rolling volatilities,
    volume changes, regime indicators, and GARCH variance.

### 4. Model Evaluation

**Statistical Metrics:**
- RMSE
- MAE
- Directional accuracy
- Out-of-sample R²

**Economic Metrics (Backtesting):**
- Cumulative returns
- Sharpe ratio
- Maximum drawdown

### 5. Robustness & Regime Analysis

-   Walk-forward validation
-   Regime segmentation (bull, bear, sideways)
-   Assessment of efficiency under varying market conditions

| Name   | Age | Score |
|:-------|:---:|------:|
| Alice  | 21  | 88.5  |
| Bob    | 19  | 91.0  |


## Hypotheses Tested
------------------------------------------------------------------------------

| Model   | Captures | EMH Hypothesis Tested |
|:-------|:---:|------:|
| **ARIMA(1,0,1)**  | Linear autocorrelation  | Weak-form EMH  |
| **GARCH(1,1)**    | Volatility clustering  | Time-varying volatility inconsistent with EMH |
| **XGBoost**    | Nonlinear dependencies  |  Predictability contradicts EMH |


  | Model             | Captures          | EMH Hypothesis Tested                    |
  |------------------ | ----------------- | -----------------------------------------|
  |**ARIMA(1,0,1)**    |Linear               | Weak-form EMH                         |
                     autocorrelation   

  |**GARCH(1,1)**    | Volatility        | Time-varying volatility inconsistent with |
                     clustering        EMH

  |**XGBoost**       | Nonlinear         | Predictability contradicts EMH            |
                     dependencies     
  ------------------------------------------------------------------------------

## Tools & Technologies

-   **Python 3.12**
-   `statsmodels` (ARIMA, diagnostic tests)
-   `arch` (GARCH modeling)
-   `xgboost`, `scikit-learn` (machine learning)
-   `pandas`, `numpy` (data processing)
-   `matplotlib` (visualization)
-   Executed in **Google Colab**

## Goals & Objectives

-   Test whether daily returns of SPX and BTC conform to weak-form EMH
-   Compare econometric and machine learning predictability
-   Convert predictions into trading strategies
-   Evaluate economic significance through backtesting
-   Analyze differences across market regimes
-   Provide insights for portfolio management and market behaviour

## Project Deliverables

-   Clean datasets and preprocessing scripts
-   ARIMA and GARCH modeling notebooks
-   XGBoost modeling notebook with feature engineering
-   Backtesting engine
-   Regime classification and robustness analysis
-   Summary report and visualizations

## Contributions

-    King Kyei Boakye – turtledovesbeloved97@gmail.com
-    Solomon Owusu Sarfo – solomonsarfo045@gmail.com

