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

