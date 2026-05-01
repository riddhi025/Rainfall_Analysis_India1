# Rainfall Analysis and Climate Variability in India

## Overview

This project analyzes historical rainfall data across different regions of India to understand long-term climate patterns, seasonal dependency, regional variability, and extreme weather behavior. It also applies statistical analysis and machine learning models to study rainfall predictability.

The objective is to go beyond basic visualization and develop meaningful insights into climate variability and rainfall dynamics in India.

---

## Objectives

- Analyze long-term rainfall trends across India
- Study seasonal distribution of rainfall and monsoon dependency
- Compare rainfall patterns across regions
- Measure rainfall variability and climate risk
- Identify extreme rainfall events
- Build machine learning models for rainfall prediction
- Study temporal dependency in rainfall patterns

---

## Dataset

- Source: Kaggle Rainfall in India dataset
- Time Period: 1901 to present
- Granularity: Monthly rainfall aggregated by region
- Features include:
  - Monthly rainfall (Jan to Dec)
  - Seasonal aggregates
  - Annual rainfall
  - Regional subdivisions

---

## Data Preprocessing

- Handled missing values using region-wise mean imputation
- Created seasonal features:
  - Winter
  - Summer
  - Monsoon
  - Post-monsoon
- Engineered lag feature (previous year rainfall)
- Validated and cleaned annual rainfall values
- Removed inconsistencies and missing data

---

## Exploratory Data Analysis

Key insights from analysis:

- Monsoon season contributes the majority of annual rainfall in India
- Rainfall shows high interannual variability
- Significant regional differences exist in rainfall patterns
- Some regions show high variability indicating higher climate risk
- Rainfall distribution is positively skewed, indicating extreme events

---

## Statistical Analysis

- Distribution analysis of annual rainfall
- Correlation between monthly rainfall patterns
- Variability measured using standard deviation across regions
- Identification of extreme rainfall years using percentile thresholds
- Skewness analysis of rainfall distribution

---

## Machine Learning Models

### Models Used

- Linear Regression
- Random Forest Regressor

### Feature Engineering

- Seasonal rainfall components
- Previous year rainfall (lag feature)

### Model Performance

| Model | R2 Score | RMSE |
|------|----------|------|
| Linear Regression | 0.84 | 378 |
| Random Forest | 0.79 | 429 |

---

## Important Observation (Data Leakage Fix)

Initial models showed very high accuracy due to inclusion of monthly rainfall features, which directly sum to annual rainfall.

After removing these features and using only seasonal components and lag features, the model produced more realistic and interpretable performance.

---

## Key Findings

- Rainfall exhibits strong temporal dependency across years
- Monsoon season dominates total rainfall in India
- Regional variability indicates uneven climate risk distribution
- Extreme rainfall events have significant impact despite low frequency
- Predictive accuracy is limited by the stochastic nature of climate systems

---

## Real-World Applications

- Agricultural planning and crop risk assessment
- Water resource management
- Flood and drought risk analysis
- Climate adaptation and policy planning

---

## Limitations

- No external climate variables such as ENSO or temperature
- Regional aggregation hides local variations
- Rainfall is highly stochastic, limiting prediction accuracy
- Dataset does not include modern satellite-based climate indicators

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
