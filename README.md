# Stock Price Forecasting with Exogenous Variables: Cross-Sector & Cross-Crisis Analysis

This project is my MSc Data Analytics thesis, investigating whether external (exogenous) variables improve stock price forecasting under different economic conditions.

The research compares statistical and deep learning models across sectors and crisis periods, focusing on when additional data improves predictive performance—and when it does not.

The project was awarded a First-Class grade (72%), included a Viva examination, and received a special mention at graduation.

---

## Project Overview

Financial forecasting becomes significantly more challenging during periods of economic disruption. This research evaluates model performance across two major shocks:

* The COVID-19 pandemic (2020–2021)
* The 2025 U.S. tariff disruption

Two companies from different sectors were analysed:

* **Dell (Technology)**
* **Boeing (Aerospace/Manufacturing)**

The core objective was to assess whether incorporating exogenous variables—such as macroeconomic, commodity, and sector-specific indicators—improves forecasting accuracy across different contexts.

---

## Objectives

* Evaluate whether exogenous variables improve forecasting performance
* Compare baseline vs exogenous-augmented models
* Identify which categories of variables add the most value
* Assess whether useful variables transfer across economic disruptions

---

## Models & Tools

### Models

* ARIMA / SARIMA
* ARIMAX / SARIMAX (with exogenous variables)
* LSTM (with and without exogenous inputs)

### Tools & Technologies

* Python (pandas, numpy, statsmodels, scikit-learn)
* TensorFlow / Keras
* pmdarima
* yfinance API

---

## Methodology

The project follows a structured analytical pipeline:

1. Data collection (stock prices + external variables)

2. Exploratory analysis and correlation assessment

3. Stationarity testing (ADF) and differencing

4. Feature selection using:

   * Correlation analysis
   * Granger causality

5. Model development:

   * ARIMA / SARIMA (baseline models)
   * ARIMAX / SARIMAX (with exogenous inputs)
   * LSTM models with grouped inputs

6. Hyperparameter tuning:

   * Auto-ARIMA
   * Grid search
   * Keras Tuner (for LSTM)

7. Forecast evaluation:

   * Time-based train/test split (80/20)
   * Forecast horizons: 1-day, 3-day, 7-day
   * Metrics: MAE, RMSE, MAPE

The focus was on **consistent, comparable evaluation across models and scenarios**, rather than optimising a single model.

---

## Key Insights

* The impact of exogenous variables is **highly context-dependent**

* Variables effective during COVID often **did not generalise** to 2025 conditions

* Sector differences are significant:

  * Dell benefited more from **commodity and supply chain indicators**
  * Boeing responded more to **sectoral and macroeconomic signals**

* Model performance depends on forecast horizon:

  * ARIMA-family models performed best at **short horizons**
  * LSTM models performed better at **longer horizons**

* Increased model complexity does not guarantee better results

---

## Key Takeaway

There is no universal “best” model or variable set — forecasting performance depends heavily on sector, disruption type, and prediction horizon.

---

## Results

Model performance varied significantly across:

* Companies
* Crisis periods
* Forecast horizons

In many cases:

* Baseline models performed comparably to models with exogenous variables
* Improvements from additional inputs were inconsistent

This highlights the importance of **model comparison, context awareness, and disciplined evaluation**.

---

## Limitations

* Financial time series are highly volatile and sensitive to external shocks
* Exogenous variables introduce additional uncertainty
* Model assumptions (e.g. stationarity) may not always hold
* Limited computational resources constrained full hyperparameter optimisation
* Results depend heavily on variable selection and data quality

---

## What I Demonstrated

* Time series modelling (ARIMA, SARIMA, LSTM)
* Feature engineering with exogenous variables
* Model evaluation and comparison across scenarios
* Data pipeline design and preprocessing
* Analytical thinking under real-world constraints
* Clear communication of complex findings

---

## Recognition

* First-Class grade (72%)
* Viva examination completed
* Special mention at graduation

---

## Repository Structure

- `Notebooks/` – model development, experiments, and analysis  
- `Data/` – processed datasets used for modelling  
- `Report/` – final thesis document  

- `reproducible_version/` – original project structure used during development.  
  This version preserves file paths and dependencies required to fully reproduce experiments without modification.

---


## Disclaimer

This project is for academic research purposes only and is not intended for financial decision-making.
The data used in this project is provided “as is” without guarantees of accuracy or completeness.  

---

## License

This project is licensed under the MIT License.

### Data & External Tools

- This project uses data sourced via the `yfinance` library, which is distributed under the Apache License 2.0.
- Financial data accessed through Yahoo Finance is subject to Yahoo’s Terms of Service and is intended for personal and academic use only.


