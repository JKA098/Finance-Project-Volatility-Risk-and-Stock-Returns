#  Project — Volatility, Risk, and Stock Returns



![Finance](https://img.shields.io/badge/Finance-Stock_Analytics-0F172A?style=for-the-badge)
![Risk](https://img.shields.io/badge/Risk-Volatility_%7C_Sharpe-7C2D12?style=for-the-badge)
![Stats](https://img.shields.io/badge/Stats-Correlation_%7C_Regression-1E3A8A?style=for-the-badge)
![R](https://img.shields.io/badge/R-RStudio-276DC3?style=for-the-badge&logo=r&logoColor=white)
![Tidyverse](https://img.shields.io/badge/Tidyverse-Data_Wrangling-4B5563?style=for-the-badge)
![ggplot2](https://img.shields.io/badge/Visualization-ggplot2-111827?style=for-the-badge)
![Data](https://img.shields.io/badge/Data-Yahoo_Finance-92400E?style=for-the-badge)
![yfinance](https://img.shields.io/badge/Python_Data-yfinance-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Methods](https://img.shields.io/badge/Methods-Returns_%7C_Volatility_%7C_Heatmap-7F1D1D?style=for-the-badge)



##  Project Overview

This project investigates a central question in financial economics:

> **Do stocks with higher volatility tend to have higher average returns over time?**

Using historical stock price data, the project applies **statistical analysis**, **visualization**, and **risk metrics** to explore the relationship between **volatility**, **average returns**, and **risk-adjusted performance** across six major U.S. stocks.

The analysis blends **theoretical finance concepts** with **practical data analysis**, making it suitable as an academic term project and a portfolio-ready example of applied financial analytics.

---

##  Research Motivation

Financial markets are inherently uncertain. Investors continuously seek strategies that balance:

*  **Return**
*  **Risk**
*  **Predictability**

Volatility is commonly used as a proxy for risk, but whether it reliably predicts higher returns remains debated. This project contributes to that discussion by combining:

* Descriptive statistics
* Correlation and regression analysis
* Risk-adjusted performance metrics (Sharpe Ratio)

---

##  Hypothesis

> **Stocks with higher volatility tend to have higher average returns over time.**

---

##  Dataset Description

###  Data Source

* Retrieved using **Python's `yfinance` library**
* Sourced from **Yahoo Finance**
* Exported to CSV and analyzed in **RStudio**

###  Stocks Analyzed

* Apple (**AAPL**)
* Amazon (**AMZN**)
* Alphabet (**GOOGL**)
* Microsoft (**MSFT**)
* Tesla (**TSLA**)
* Visa (**V**)

###  Time Period

* From **2010 onward** (varies by stock availability)

###  Key Columns Used

| Field     | Description                            |
| --------- | -------------------------------------- |
| Date      | Trading day                            |
| Close     | **Primary variable used** for analysis |
| Adj.Close | Adjusted closing price                 |
| High      | Daily high price                       |
| Volume    | Shares traded                          |

> The **Close** price was used to compute daily returns, volatility, correlations, and risk metrics.

---

##  Tools & Libraries

### R Libraries Used

```r
tidyverse
knitr
kableExtra
GGally
corrplot
TTR
forecast
ggplot2
```

### Document Configuration

* Quarto PDF output
* Controlled float placement for tables and figures
* Figures stored in a dedicated `figures/` directory

---

##  Methodology

### 1️⃣ Data Preparation

* Imported CSV into R
* Selected all `Close` columns using `grep()`
* Converted all price columns to numeric
* Handled missing values using `na.rm = TRUE`

---

### 2️⃣ Descriptive Statistics

Calculated for each stock:

* **Mean price**
* **Variance**
* **Standard deviation (volatility)**

Results were combined into a clean summary table for comparison.

---

### 3️⃣ Return & Volatility Calculation

Daily returns were computed alongside the following:

* **Average return (mean of daily returns)**
* **Volatility (standard deviation of daily returns)**

---

### 4️⃣ Visualization

* Scatterplots of **Volatility vs Average Return**
* Labeled points for each stock
* Enhanced visualization using `ggplot2`

---

### 5️⃣ Correlation Analysis

* Pearson correlation between:

  * Volatility and average returns
* Correlation matrix across all stocks
* Heatmap visualization using `corrplot`

---

### 6️⃣ Regression Analysis

A linear regression model was fitted and Evaluated using:

* R-squared
* P-value
* Regression visualization

---

### 7️⃣ Risk Metrics — Sharpe Ratio

Risk-adjusted performance was measured alongside the following:


* `Risk-free rate` was assumed at **1%**
* and calculated individually for each stock

---

## Key Results

### Volatility vs Returns

* **Strong positive relationship**
* Correlation ≈ **0.99**
* **TSLA** showed both the highest volatility and highest average return

### Regression Findings

* **R² ≈ 0.985**
* **Statistically significant relationship**
* Volatility explains ~98.5% of return variability

### Correlation Matrix

* Strong co-movement among tech stocks (MSFT, GOOGL)
* TSLA exhibited weaker correlations, suggesting diversification potential

### Sharpe Ratio Results

* All stocks had **negative Sharpe ratios**
* Indicates underperformance relative to a 1% risk-free rate
* TSLA performed *best relative to risk*, despite being negative



## Discussion & Interpretation

* Results **support the hypothesis**: higher volatility is associated with higher average returns.
* However, **risk-adjusted returns were poor**, highlighting an important trade-off:

  * High returns do not necessarily justify high risk.
* Volatility alone is **not sufficient** as a stock selection metric.

---

## Limitations

* Daily returns used instead of annualized metrics
* Volatility measured only as standard deviation
* Limited number of stocks
* Assumed constant risk-free rate

---

## Future Work

* Annualized volatility and returns
* Alternative risk measures (Sortino Ratio, Drawdowns, CED)
* Portfolio-level analysis
* Time-varying volatility models
* Sector-based comparison






