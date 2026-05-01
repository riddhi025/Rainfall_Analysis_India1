# Rainfall Analysis and Climate Variability in India

## Overview

This study investigates rainfall variability in India using historical precipitation data to understand long-term trends, seasonal concentration, regional disparities, and temporal dependencies in rainfall behavior.

The primary focus is to evaluate whether rainfall patterns exhibit **temporal persistence** and whether **previous-year rainfall can explain interannual variability** across different regions.

Rather than treating this as a purely predictive task, the project emphasizes **climate interpretation, statistical behavior, and system-level understanding of rainfall dynamics**.

---

## Research Objective

This project addresses the following key question:

- To what extent does rainfall in India exhibit temporal dependency, and how well can previous-year rainfall explain current-year rainfall variability across regions?

Secondary objectives include:

- Understanding long-term rainfall trends in India  
- Analyzing seasonal concentration and monsoon dominance  
- Studying regional variability and climate risk distribution  
- Identifying extreme rainfall behavior and distribution skewness  
- Evaluating predictive limits of rainfall modeling

---

## Dataset

- Source: Kaggle Rainfall in India dataset  
- Time Period: 1901 – Present  
- Granularity: Monthly rainfall aggregated by region  
- Features:
  - Monthly rainfall (Jan–Dec)
  - Seasonal aggregates (Winter, Summer, Monsoon, Post-monsoon)
  - Annual rainfall
  - Regional subdivisions

---

## Data Preprocessing

- Missing values handled using region-wise mean imputation  
- Seasonal features constructed:
  - Winter
  - Summer
  - Monsoon
  - Post-monsoon  
- Lag feature engineered:
  - Previous-year rainfall (`prev_year`)  
- Data cleaned for inconsistencies and duplicates  

---

## Exploratory Data Analysis

### Key Observations

- Rainfall exhibits strong interannual variability with no stable long-term mean pattern  
- Monsoon season dominates total annual rainfall contribution  
- Significant regional disparities exist in rainfall magnitude and variability  
- Rainfall distribution is positively skewed, indicating frequent extreme events  

---

## Statistical Analysis

- Distribution analysis of annual rainfall shows high variability across years  
- Correlation structure reveals strong dependence between seasonal components  
- Standard deviation across regions highlights uneven climate risk distribution  
- Extreme rainfall years identified using percentile-based thresholds  
- Skewness confirms higher probability of extreme high-rainfall events  

---

## Machine Learning Models

### Models Used

- Linear Regression  
- Random Forest Regressor  

### Feature Engineering

- Seasonal rainfall components  
- Previous-year rainfall (lag feature)

---

## Model Performance

| Model | R² Score | RMSE |
|------|----------|------|
| Linear Regression | 0.84 | 378 |
| Random Forest | 0.79 | 429 |

---

## Key Insight from Modeling

The Linear Regression model outperforms Random Forest, indicating that rainfall exhibits a largely **linear and temporally persistent structure**.

The inclusion of `prev_year` reveals a strong **temporal autocorrelation**, suggesting that past rainfall significantly influences current-year rainfall.

However, approximately 16% of variability remains unexplained, indicating the influence of external climatic drivers not included in the dataset.

---

## Important Observation: Data Leakage

Initial models showed artificially high accuracy due to inclusion of monthly rainfall variables, which directly aggregate into annual rainfall.

After removing these features and relying only on seasonal components and lag-based features, the model produced more realistic and interpretable results.

This correction highlights the importance of avoiding **feature leakage in climate modeling problems**.

---

## Key Findings

- Rainfall in India shows strong temporal dependency across years  
- Monsoon is the dominant driver of annual precipitation  
- Regional rainfall variability is significantly higher than national averages suggest  
- Extreme rainfall events contribute disproportionately to overall distribution behavior  
- Predictive accuracy is fundamentally limited by missing external climate drivers  

---

## Scientific Interpretation

Rainfall in India behaves as a partially persistent system where historical values provide meaningful predictive power. However, the system remains highly stochastic due to unmodeled atmospheric and oceanic influences.

The presence of temporal autocorrelation (R² ≈ 0.84) suggests that rainfall dynamics are not purely random but are influenced by slow-evolving climatic conditions.

---

## Real-World Applications

- Agricultural risk forecasting  
- Water resource planning  
- Flood and drought risk assessment  
- Climate adaptation strategies  
- Regional environmental planning  

---

## Limitations

- No external climate variables (ENSO, temperature, humidity, pressure systems)  
- Regional aggregation masks local-scale variability  
- Rainfall is inherently stochastic, limiting deterministic prediction  
- Dataset lacks modern satellite-based climate observations  

---

## Future Work

- Incorporate climate indices such as ENSO and Indian Ocean Dipole  
- Use time series models (ARIMA, LSTM) for temporal forecasting  
- Introduce spatial clustering of rainfall zones  
- Integrate satellite-based precipitation datasets  
- Improve modeling using exogenous climate variables  

---

## Tech Stack

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Scikit-learn  
- SciPy  

---

## Author

Riddhi Bhattacharya  
B.Tech Student | Data Science and Climate Analytics Enthusiast  

---

## Acknowledgements

Dataset sourced from Kaggle. This project is intended for educational and research exploration of climate data.
