# Data Analysis & Modeling

**Folder:** `1_analysis/`  
**Primary Output:** `Analysis.ipynb`  

This directory contains the analysis code and notebooks used to study the determinants of Foreign Direct Investment (FDI) across developing economies. All work in this folder uses cleaned datasets stored in `0_datasets/` and is designed to be fully reproducible.

---

## Research Question

**Which structural, macroeconomic, and institutional variables most strongly explain FDI inflows in developing economies?**

---

## Reproducibility & Open Science

This folder follows strict read-only and reproducible workflows:

- **Input:** Scripts read from the prepared panel datasets in `0_datasets/`  
  - `panel_innerjoin_strict.csv`  
  - `panel_full_left_join.csv`  
- **Process:** All transformations for modeling (e.g., log transforms, lag variables, filtered subsets) are performed in memory using pandas DataFrames.  
- **Output:** No script in this folder overwrites or edits any file in `0_datasets/`. Any additional outputs (figures, tables) are saved into analysis- or results-specific locations.

---

## Methodological Framework

The analysis follows a structured pipeline: expectation → observation → critique.

### 1. Data Loading and Integrity Checks

Before modeling, the notebook:

- Loads the balanced regression panel and the wider left-join panel.
- Confirms the panel structure (number of countries and years).
- Checks for:
  - Missing values and sparsity, especially in institutional indicators.
  - Consistent units (e.g., percentages vs raw levels).
  - Basic distribution properties (skewness, outliers, heavy tails).

### 2. Exploratory Diagnostics

The notebook runs several diagnostic steps to understand the data structure:

- **Univariate distributions:**  
  Histograms and density plots for FDI and key predictors (GDP growth, trade, inflation, logistics, electricity, education).

- **Bivariate patterns:**  
  Scatter plots and simple trend lines to see how FDI co-moves with GDP growth, LPI score, and other variables.

- **Correlation and multicollinearity:**  
  - Correlation matrix for all numeric variables.  
  - Visual heatmap to detect high correlations.  
  - Used to inform which variables may be redundant in regression.

---

## Regression Modeling

### 1. Pooled OLS Regression

The main regression model uses log FDI as the dependent variable:

Model Specification (Equation Format):

log(FDI_it) =
    β0
    + β1 * GDP_growth_it
    + β2 * Trade_pct_GDP_it
    + β3 * Inflation_CPI_it
    + β4 * LPI_score_it
    + β5 * CPI_it
    + β6 * Electricity_access_it
    + β7 * Education_enrollment_it
    + ε_it

Key Regressors Included:
- GDP growth
- Trade openness (% of GDP)
- Inflation (CPI)
- Logistics Performance Index (LPI)
- Corruption Perception Index (CPI)
- Electricity access
- Education enrollment


Key implementation details:

- Estimated using `statsmodels` OLS.  
- Cluster-robust standard errors at the country level to handle:
  - Heteroskedasticity.
  - Serial correlation within each country over time.

The notebook reports:

- Coefficient estimates and signs.  
- p-values and confidence intervals.  
- Overall model fit (R², Adjusted R²) and specification diagnostics.

*(A country- and year-fixed-effects version was explored, but final reporting focuses on the pooled specification with clustering, due to limited sample size.)*

---

## Machine Learning Modeling

### 1. Random Forest Regressor

To complement the regression and focus on prediction rather than interpretation, the notebook trains a Random Forest model with:

- **Target:**  

log(FDI_it)

- **Predictors:**  
  - GDP_growth  
  - Trade_pct_GDP  
  - Inflation_CPI  
  - LPI_score  
  - CPI  
  - Electricity_access  
  - Education_enrollment  
  - A lagged FDI term:  
        log(FDI_i,t-1)


The model uses a standard train–test split (e.g., 80% / 20%) and reports:

- R² on the test set.  
- Mean Absolute Error (MAE).  
- Root Mean Squared Error (RMSE).  

The notebook also generates a **feature importance plot**, showing which predictors contribute most to out-of-sample prediction.

---

## Main Empirical Results

### 1. Correlation Analysis

From the correlation matrix:

- **GDP size** (country_GDP_size) is strongly correlated with FDI.  
- **LPI_score** (logistics performance) has a moderate positive correlation with FDI.  
- **Electricity_access** is positively correlated with FDI, consistent with infrastructure being a basic requirement.  

These are raw associations and do not control for other variables.

### 2. Regression Results (Pooled OLS)

Once we control for multiple variables at the same time, the pooled OLS model suggests:

- **Statistically significant positive predictors (p < 0.05):**  
  - Logistics Performance Index (LPI_score).  
  - Electricity_access.  
  - Inflation_CPI (interpreted carefully as capturing high-growth or reform episodes).

- **Not statistically significant in this specification:**  
  - GDP_growth (short-run fluctuations).  
  - Trade_pct_GDP.  
  - Education_enrollment.  
  - CPI (corruption) in the presence of other structural variables.

Interpretation:

- Structural, physical factors (logistics and electricity) remain robust drivers of FDI once we control for other covariates.  
- Pure year-to-year GDP growth and trade openness matter less than long-run market size and the ability to operate efficiently.

### 3. Machine Learning Results (Random Forest)

The Random Forest model highlights a different aspect:

- The **lagged FDI** term is the single most important feature for predicting current FDI.  
  - This indicates strong persistence or “stickiness” in investment patterns: where capital goes once, it tends to return.  

- Among structural variables, **electricity access** and **logistics performance** remain among the top contributors to prediction.

- Some variables that appear weak or insignificant in OLS still contribute in the Random Forest because it can exploit non-linearities and interactions without requiring stable linear coefficients.

---

## File Summary

### `Analysis.ipynb`

This notebook contains the full analysis pipeline. Major sections:

1. **Setup and Data Loading**  
   - Imports required libraries.  
   - Loads `panel_innerjoin_strict.csv` and `panel_full_left_join.csv` from `0_datasets/`.

2. **Descriptive Diagnostics**  
   - Summary tables for key variables.  
   - Exploration of missing values.  
   - Basic plots for distributions and trends.

3. **Correlation Analysis**  
   - Correlation matrix for numeric variables.  
   - Heatmap to visualize relationships.

4. **Econometric Modeling (OLS)**  
   - Log-transform of FDI.  
   - Pooled OLS regression with cluster-robust standard errors.  
   - Interpretation of key coefficients.

5. **Machine Learning Modeling (Random Forest)**  
   - Construction of lagged FDI feature.  
   - Train–test split and model training.  
   - Evaluation metrics and feature importance visualization.

6. **FDI Patterns Over Time and Space**  
   - Country profiles (FDI + GDP growth over time).  
   - Time-series plots of global average FDI.  
   - Choropleth map of FDI by country and year (Plotly).

---

