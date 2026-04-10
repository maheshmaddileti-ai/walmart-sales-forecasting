# Walmart Sales Forecasting

Retail sales forecasting project analyzing weekly sales data across 45 Walmart stores to identify revenue drivers and predict future sales using machine learning.

---

## Problem Statement

A retail chain with multiple outlets across the country faces challenges in managing inventory to match demand with supply. This project uses historical weekly sales data to uncover insights and build predictive models that forecast sales for each store.

---

## Dataset

**File:** `Walmart_Dataset.csv`  
**Rows:** 6,435  
**Columns:** 8

| Feature | Description |
|---|---|
| Store | Store number (1–45) |
| Date | Week of sales |
| Weekly_Sales | Sales for the given store that week |
| Holiday_Flag | Whether it was a holiday week (1 = Yes) |
| Temperature | Temperature on the day of sale |
| Fuel_Price | Cost of fuel in the region |
| CPI | Consumer Price Index |
| Unemployment | Unemployment rate in the region |

---

## Project Objectives

1. Find useful insights from the data that each store can use to improve performance
2. Forecast weekly sales for each store for the next 12 weeks

---

## Key Findings

- **Unemployment vs Sales:** Unemployment rate shows a negative correlation with weekly sales — stores in high-unemployment regions consistently underperform
- **Seasonal Trends:** Holiday weeks (Thanksgiving, Christmas) show significant sales spikes of 15–20% above average
- **Top Stores:** Stores 20, 4, and 14 are the highest revenue generators historically
- **Temperature Impact:** Mild temperature ranges correlate with higher sales; extreme cold reduces footfall
- **CPI Effect:** Rising CPI (inflation) is associated with reduced discretionary spending across stores

---

## Models Built

| Model | Type |
|---|---|
| Linear Regression | Baseline |
| Decision Tree Regressor | Tree-based |
| Random Forest Regressor | Ensemble |
| K-Nearest Neighbors | Instance-based |
| XGBoost Regressor | Gradient Boosting |
| **Ensemble (DT + RF + XGB)** | **Final Model** |

The final prediction averages the top 3 models (Decision Tree, Random Forest, XGBoost) for improved accuracy.

---

## Techniques Used

- IQR-based outlier removal
- Mean imputation for missing values
- Seasonal decomposition (trend, seasonal, residual)
- T-test to compare holiday vs non-holiday sales
- Feature importance using Random Forest
- Store-level correlation analysis with unemployment rate

---

## Tech Stack

- **Language:** Python 3
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, XGBoost, Statsmodels, SciPy

---

## Project Structure

```
walmart-sales-forecasting/
│
├── walmart_project.py        # Main analysis and modeling code
├── Walmart_Dataset.csv       # Dataset
└── README.md                 # Project documentation
```

---

## How to Run

1. Clone the repository
```bash
git clone https://github.com/maheshmaddileti/walmart-sales-forecasting
```

2. Install dependencies
```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost statsmodels scipy
```

3. Run the script
```bash
python walmart_project.py
```

> Note: If running in Google Colab, update the file path in `pd.read_csv()` to point to your uploaded dataset.

---

## Author

**Mahesh Maddileti**  
PGP in Data Science & Machine Learning — IntelliPaat (April 2026)  
[LinkedIn](https://linkedin.com/in/maheshmaddileti) | [GitHub](https://github.com/maheshmaddileti)

---

## Certificate

This project was completed as part of the IntelliPaat Post Graduate Program in Data Science & Machine Learning.  
Certificate ID: 31679-462158-209407
