# 🏏 IPL Player Performance Prediction — Capstone Project

## 📌 Executive Summary

This project predicts the **total runs** a batsman is expected to score in an IPL season using historical **ball-by-ball match data**. The objective is to provide valuable insights to analysts, franchise decision-makers, and fans by identifying performance trends from previous seasons.

We engineered season-level features such as **balls faced**, **strike rate**, and **matches played**, and evaluated several machine learning models to assess predictive performance.

---

## 🧠 Business Context

In the Indian Premier League (IPL), accurately forecasting player performance is crucial for team composition, auction strategy, and fan engagement. This project demonstrates how historical performance data can be harnessed to make data-informed decisions. By predicting seasonal run totals, franchises can discover undervalued talent, optimize their rosters, and gain a competitive edge.

---

## 📂 Project Structure

- `README.md`: Project overview, objectives, and high-level findings.
- `ipl_Runs_per_season_EDA_and_Visualization.ipynb`: Exploratory data analysis, feature engineering, and initial modeling.
- `IPL_Final_Project.ipynb`: Final models including Ridge, Random Forest, and XGBoost with GridSearchCV, along with comparison insights.

---

## 📊 Results Overview

| Model             | Val MAE | Val RMSE | Val R² | Test MAE | Test RMSE | Test R² |
|------------------|---------|----------|--------|----------|-----------|---------|
| Linear Regression | 16.05   | 23.85    | 0.98   | 17.34    | 30.12     | 0.97    |
| Ridge Regression  | 15.94   | 23.86    | 0.98   | 17.53    | 30.32     | 0.97    |
| Random Forest     |  2.75   |  7.56    | 1.00   |  3.34    |  9.79     | 1.00    |
| XGBoost           |  2.58   |  4.51    | 1.00   |  3.00    |  5.94     | 1.00    |

🔍 **XGBoost** delivered the best performance, but additional validation is recommended to check for feature leakage or overfitting.

---

## 🧪 Modeling Approach

- Cleaned and explored IPL ball-by-ball match data
- Aggregated to player-season level
- Engineered features including:
  - `balls_faced`, `strike_rate`, `matches_played`
  - Previous season statistics
  - One-hot encoded team indicators
- Applied and compared multiple models:
  - Linear Regression (baseline)
  - Ridge Regression
  - Random Forest
  - XGBoost
- Time-based split:
  - **Train**: ≤ 2021  
  - **Validation**: 2022  
  - **Test**: 2023

---

## 📈 Visualizations

- Distributions of player performance metrics
- Season trends and player consistency
- Home vs Away performance
- Correlation heatmaps and scatter plots
- Actual vs Predicted Runs for Top 10 Batters
- Residuals (distribution and error patterns)
- Feature importance (Ridge coefficients, Random Forest, XGBoost)

---

## 🔍 Key Findings

- `balls_faced` is the most predictive feature across models.
- Linear models perform well but miss non-linear patterns.
- Ensemble models (XGBoost, Random Forest) achieve near-perfect fit—additional tests needed to rule out overfitting.
- Team-level features contribute modestly; future work could include contextual features (e.g., opposition, venue, match phase).

---

## 🔄 Next Steps

- Add contextual features: opponent, venue, recent form
- Incorporate SHAP for better interpretability
- Build per-match or per-phase prediction models
- Validate further for feature leakage or label contamination

---

## ✅ Submission Checklist

- [x] Organized notebook with markdown headers
- [x] Clear variable naming and clean code
- [x] Readable and well-labeled visualizations
- [x] Multiple models with validation/test results
- [x] Business-friendly summary and actionable next steps

---

## 💬 Author

Capstone project submitted as part of the **[Berkeley ML & AI Professional Certificate Program]**
