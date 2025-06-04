# Bank Marketing Classifier Comparison

## 📌 Objective
This project evaluates and compares the performance of multiple classification algorithms on a bank marketing dataset. The goal is to predict whether a client will subscribe to a term deposit based on their demographic and interaction history.

---

## 🧠 Problem Overview

We compare the following classifiers:
- Logistic Regression
- K-Nearest Neighbors (KNN)
- Decision Tree
- Support Vector Machine (SVM)

Each model is evaluated using:
- Grid search for hyperparameter tuning
- Feature-engineered inputs
- Train/Test accuracy
- F1-score, Recall
- ROC-AUC and Confusion Matrix

---

## ⚙️ Feature Engineering

Engineered features include:
- `was_previously_contacted`: binary indicator derived from `pdays`
- `prev_success`: combination of `previous` and `poutcome`
- `month_sin`, `month_cos`: cyclical encoding of `month`
- `day_sin`, `day_cos`: cyclical encoding of `day_of_week`
- Binned `age` into categories (e.g., young, middle-aged, senior)

The `default` column was dropped due to extreme imbalance and high proportion of "unknown" values.

---

## 🧪 Model Evaluation

| Model               | Test Accuracy | AUC  | Train Time |
|--------------------|---------------|------|------------|
| Decision Tree       | 0.901         | 0.796 | 8.59s      |
| Logistic Regression | 0.900         | 0.793 | 9.82s      |
| SVM (sampled data)  | 0.899         | —     | 9.34s      |
| KNN                 | 0.898         | —     | 35.24s     |

> Note: SVM was trained on a 5K-row subsample due to high computational cost on full data.

---

## 📊 Metrics & Visualization
- ROC curves showed similar performance for Logistic Regression and Decision Tree.
- F1-score and Recall were used to validate performance under class imbalance.
- Confusion matrices provided insight into false positive/negative rates.

---

## 🔚 Next Steps
- Optimize decision threshold for better recall.
- Try ensemble models like Random Forest or Gradient Boosting.
- Evaluate cost-sensitive learning if false negatives are expensive.
- Deploy the top-performing model with feature pipeline.

---

## 🧑‍💻 Author
Suresh Venkatesan
