<<<<<<< Updated upstream
# 📊 IPL Runs Prediction Capstone

## 🗂️ Project Overview

This capstone project aims to **predict the total runs a player will score in an IPL season** using historical ball-by-ball IPL data. By aggregating player-level and season-level statistics, the project builds a regression model to estimate seasonal runs, helping understand player performance and key predictive factors.

---

## 🔍 Key Findings

- **Player participation `matches_played`, `balls_faced`, and `strike_rate` are strong predictors of total seasonal runs.**
- **Previous season participation shows some correlation with next season performance.**
- Home vs Away analysis shows most players play and score more in away games, but per-match efficiency can vary.
- The baseline **Linear Regression model achieved an MAE of ~15.5 runs and an R² of 0.98**, indicating high predictive accuracy for this dataset and feature set.

---

## 🛠️ What This Repository Contains

✅ Cleaned dataset preparation scripts and EDA.  
✅ Comprehensive visualizations:
- Distributions, player performance, season trends.
- Home vs Away analysis.
- Correlation heatmaps and scatter plots.

✅ Feature engineering for player-season level modeling:
- Matches played, balls faced, strike rate, previous season matches.

✅ Baseline regression modeling:
- Linear Regression with MAE, RMSE, and R² evaluation.


## 📂 File Organization

- `README.md`: Project summary (this file).
- `ipl_runs_prediction.ipynb`: Main notebook with EDA, visualizations, feature engineering, and modeling.

---

## ✅ Summary

- The project:
  - Includes a **clear summary of findings.**. See section **Project EDA and Data Cleaning Summary**
  - Uses a **clean, organized notebook with headings and narrative.**
  - Uses clear, descriptive file naming for easy navigation.

---

## 📈 Next Steps (Optional for Capstone)

- Explore advanced regression models.
- Include feature importance analysis for interpretability.
- Experiment with additional features (batting position, venue factors).

---

Thank you for reviewing this capstone submission!
=======
# 🏏 IPL Player Performance Prediction — Capstone Project
>>>>>>> Stashed changes

## 📌 Project Summary

This project aims to predict the **total runs** a batsman will score in an IPL season using historical **ball-by-ball match data**. The goal is to help analysts, franchises, and fans understand expected player performance based on prior seasons' trends.

We used season-level aggregated features like **balls faced, strike rate, matches played**, and historical season stats to build and compare multiple predictive models.

---

## 🧠 Business Understanding

In the Indian Premier League (IPL), predicting player performance is critical for team selection, auction strategy, and fan engagement. This project simulates how teams might leverage historical data to forecast player success in a season. A model that predicts seasonal run totals can guide squad-building decisions and uncover undervalued talent.

---

## 📊 Key Results

| Model             | Val MAE | Val RMSE | Val R² | Test MAE | Test RMSE | Test R² |
|-------------------|---------|----------|--------|----------|-----------|---------|
| Linear Regression | 16.05   | 23.85    | 0.98   | 17.34    | 30.12     | 0.97    |
| Ridge Regression  | 15.94   | 23.86    | 0.98   | 17.53    | 30.32     | 0.97    |
| Random Forest     |  2.75   |  7.56    | 1.00   |  3.34    |  9.79     | 1.00    |
| XGBoost           |  2.58   |  4.51    | 1.00   |  3.00    |  5.94     | 1.00    |

🔍 **XGBoost** delivered the best predictive performance with near-perfect accuracy, but further leakage checks are recommended before deployment.

---

## 🧪 Modeling Approach

- **Data cleaning and EDA** on ball-by-ball IPL dataset
- Aggregation to player-season level
- Feature engineering: `balls_faced`, `strike_rate`, `matches_played`, previous season stats, and one-hot encoded teams
- Models used:
  - Linear Regression (baseline)
  - Ridge Regression (regularized)
  - Random Forest Regressor
  - XGBoost Regressor
- **Train/Validation/Test split** based on year:
  - Train: ≤ 2021
  - Validation: 2022
  - Test: 2023

---

## 📈 Visualizations

- Top 10 run-scorers: Actual vs Predicted
- Residual plots (distribution, predicted vs actual)
- Feature importance (Ridge coefficients, Random Forest, XGBoost)

---

## 🔍 Key Findings

- `balls_faced` is the most influential predictor across all models.
- Linear models were effective but limited in capturing non-linearity.
- XGBoost and Random Forest significantly reduced error but may be overfitting due to near-perfect R².
- Team-based features had minor influence — future work can explore role-specific or venue-based features.

---

## 🔄 Next Steps

- Add more contextual features: opposition, venue, recent form
- Use SHAP values for better model explainability
- Build per-match or per-phase (e.g., powerplay) prediction models
- Reassess for possible feature leakage or target contamination

---

## 📁 Files Included

- `ipl_runs_prediction.ipynb`: Full notebook with code, EDA, modeling, and visualizations
- `README.md`: Summary of approach and findings

---

## ✅ Submission Checklist

- [x] Organized notebook with markdown headers
- [x] All libraries and variables named clearly
- [x] Clean visualizations with readable axes and labels
- [x] Multiple models with validation/test metrics
- [x] Clear summary and next steps for nontechnical readers

---

## 💬 Author

Capstone project submitted as part of the [Berkeley ML & AI Professional Certificate Program].
