# 🏠 King County House Price Prediction

## Overview
This project predicts residential property sale prices in King County, Washington 
using real official data from the King County Assessor's Office. 
Unlike toy datasets, this project works with over 1 million real estate 
transaction records merged from multiple official sources.

## Data Sources
All data is publicly available from the King County Assessor's Office:
👉 info.kingcounty.gov/assessor/datadownload/default.aspx

- **Real Property Sales** — 2.4M+ actual sale transactions
- **Residential Building** — Building characteristics (size, grade, year built)
- **Parcel** — Land and location features (view, waterfront, township)

## Project Steps
- Merging 3 official datasets using Major & Minor parcel keys
- Data cleaning (removing non-arms-length sales, outliers, zero values)
- Exploratory Data Analysis (EDA) with visualizations
- Log transformation of skewed target variable
- Feature selection via correlation analysis
- Linear Regression (baseline) → XGBoost (final model)

## Results
| Model | R² | MAE |
|---|---|---|
| Linear Regression | 0.30 | 0.49 |
| XGBoost | 0.50 | 0.38 |

## Key Finding
**PrincipalUse** (property use type) was the strongest predictor of sale price, 
followed by **BldgGrade** (construction quality) and **PropertyType**.

## Tools
Python, Pandas, Scikit-learn, XGBoost, Matplotlib, Seaborn
