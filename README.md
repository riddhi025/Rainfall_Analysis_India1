# Rainfall Pattern Analysis & Prediction in India

## Overview
This project analyzes historical rainfall data across India to understand long-term trends, regional variability, and climate risks. It also builds machine learning models to predict annual rainfall using temporal features.

## Objectives
- Analyze rainfall trends over time
- Study seasonal and regional variability
- Model rainfall using statistical and ML techniques
- Identify climate risks and extreme events

## Dataset
- Source: Kaggle (Rainfall in India dataset)
- Time span: 1901–present
- Features: Monthly rainfall, seasonal aggregates, regions

## Key Insights

-  Monsoon contributes the majority of annual rainfall
-  Rainfall shows high interannual variability
-  Certain regions exhibit high climate risk (high variability)
-  Strong temporal dependency (previous year rainfall influences current year)

## Machine Learning

### Models Used:
- Linear Regression
- Random Forest

### Key Finding:
- Initial models showed high accuracy due to data leakage
- After removing leakage, realistic performance achieved:
  - R² ≈ 0.84 using previous year rainfall

### Evaluation Metrics
- Root Mean Squared Error (RMSE)
- R² Score

## Visualizations
- Correlation heatmap
- Residual distribution plots
- Feature importance analysis

## Tech Stack
- Python 
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn

## Limitations
- No external climate variables (ENSO, temperature, etc.)
- Regional aggregation hides local variations
- Rainfall is inherently stochastic

## Real-World Impact
- Helps understand climate variability
- Useful for agricultural planning
- Helps to identify high-risk regions
