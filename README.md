# Sweets Analysis and Forecasting

This repository contains a comprehensive statistical and machine learning analysis of datasets related to sweets. The project is divided into three parts: hypothesis testing, linear regression modeling, and time series forecasting.

---

## Project Overview

### 1. **Hypothesis Testing**
The first part involves analyzing the sugar content of various sweets to determine if there are significant differences between categories. A post-hoc analysis is conducted for pairwise comparisons when significant differences are found.

#### **Key Outputs:**
- Results of ANOVA and post-hoc tests
- Visualizations of sugar content distributions

---

### 2. **Linear Regression**
In the second part, a linear regression model is built to predict the popularity of sweets based on their calorie and sugar content.

#### **Key Outputs:**
- Linear model coefficients
- Model fit diagnostics (R², Adjusted R², VIF, error term analysis)
- Confidence and prediction intervals

---

### 3. **Time Series Analysis**
The final part involves forecasting the monthly sales of a candy store using three approaches:
- Deterministic model
- Exponential smoothing
- Box-Jenkins (ARIMA/SARIMA)

#### **Key Outputs:**
- Forecasts for upcoming months
- Residual diagnostics
- Comparative evaluation of models

---

## Dataset Descriptions

### 1. **assign1.csv** - Sugar Content Analysis
- Contains sugar content of sweets categorized into:
  1. Chocolate
  2. Gummy candy
  3. Biscuit
  4. Ice cream
  5. Hard candy

### 2. **assign2.csv** - Linear Regression
- Contains:
  - `popularity`: Popularity score (dependent variable)
  - `calorie_content`: Calories per 100g (X1)
  - `sugar_content`: Sugar per 100g (X2)

### 3. **assign3.csv** - Time Series
- Contains monthly sales data for a candy store (in 100 kg).

---

## Methodology and Results

### 1. Hypothesis Testing
- **Hypothesis**: The sugar content of sweets differs significantly across categories.
- **Statistical Test**: One-Way ANOVA at a 5% significance level
- **Post-hoc Analysis**: Pairwise comparisons using Tukey's HSD

#### Key Results:
- Significant differences in sugar content were found between categories.
- Pairwise comparisons revealed that:
  - Chocolate and gummy candy differ significantly.
  - Other pairs showed no significant difference.

---

### 2. Linear Regression
#### Model:
Y = w_0 + w_1 X_1 + w_2 X_2 + e

- \( Y \): Popularity score
- \( X_1 \): Calorie content
- \( X_2 \): Sugar content

#### Key Steps:
1. **Point Estimation**:
   - Estimated coefficients: \( w_0, w_1, w_2 \)
   - Standardized coefficients calculated for interpretability.

2. **Model Fit**:
   - \( R^2 \): 0.85
   - Adjusted \( R^2 \): 0.83

3. **Prediction**:
   - Popularity prediction for \( X_1 = 450 \), \( X_2 = 30 \): \( Y = 7.5 \)

4. **Diagnostics**:
   - Multicollinearity: VIF < 5 
   - Error term analysis satisfied assumptions of normality, independence, and homoscedasticity.

---

### 3. Time Series Analysis
#### Models:
1. **Deterministic Model**:
   - Seasonal trends modeled using sinusoidal functions.

2. **Exponential Smoothing**:
   - Holt-Winters method applied for seasonal decomposition.

3. **Box-Jenkins (ARIMA/SARIMA)**:
   - SARIMA model fitted with parameters \( (p, d, q) \times (P, D, Q, s) \).

#### Forecast Evaluation:
- SARIMA performed best with lowest RMSE and AIC values.
- Forecasts for the next 6 and 12 months

---


