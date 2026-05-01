# Rainfall Analysis of India (Exploratory Data Analysis Project)

## Project Overview
This project performs an exploratory data analysis on rainfall patterns across India. The objective is to understand how rainfall varies across different regions and time periods and to extract meaningful insights from historical meteorological data.

The analysis can support applications in agriculture planning, water resource management, and climate studies.

---

## Objective
The main objectives of this project are:

- Analyze rainfall trends over time
- Study seasonal and regional variability
- Model rainfall using statistical and ML techniques
- Identify climate risks and extreme events

---

## Dataset Information
- Source: Kaggle (Rainfall in India dataset)
- Time span: 1901–present
- Features: Monthly rainfall, seasonal aggregates, regions

---

## Approach

### 1. Data Loading and Cleaning
- Imported dataset using Pandas  
- Handled missing values if present  
- Standardized column formats  

### 2. Exploratory Data Analysis
- Analyzed rainfall distribution across states  
- Studied seasonal variations (monsoon vs non-monsoon periods)  
- Compared rainfall trends across years  
- Identified high and low rainfall regions  

### 3. Data Visualization
The following visualizations were used:
- Bar plots for state-wise rainfall comparison  
- Line plots for trend analysis over time  
- Heatmaps for seasonal and correlation analysis  
- Distribution plots for rainfall variability  

---

### Models Used:
- Linear Regression
- Random Forest

### Key Finding:
- Initial models showed high accuracy due to data leakage
- After removing leakage, realistic performance achieved:
  - R² ≈ 0.84 using previous year rainfall
  - 
## Key Insights

- Monsoon contributes the majority of annual rainfall
- Rainfall shows high interannual variability
- Certain regions exhibit high climate risk (high variability)
- Strong temporal dependency (previous year rainfall influences current year)

## Limitations
- No external climate variables (ENSO, temperature, etc.)
- Regional aggregation hides local variations
- Rainfall is inherently stochastic

## Real-World Impact
- Helps understand climate variability
- Useful for agriculture planning
- Identifies high-risk regions

## Project Structure

-Rainfall_Analysis_India1/
-notebooks containing analysis
-dataset files
-images/ plots and visualizations
-README.md Project documentation

## Technologies Used

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Jupyter Notebook  

---

