# ✈️ NASA Predictive Maintenance using Random Forest Regression

## 📌 Project Overview

This project predicts the **Remaining Useful Life (RUL)** of aircraft engines using the **NASA CMAPSS Turbofan Engine Degradation Simulation Dataset**. The objective is to estimate how many operational cycles remain before an engine reaches failure, enabling predictive maintenance and reducing unexpected downtime.

A **Random Forest Regressor** was trained and optimized using feature importance analysis, manual hyperparameter tuning, and GridSearchCV.

---

## 🎯 Problem Statement

Traditional maintenance schedules often replace components either too early or after failure. Predictive Maintenance aims to estimate the remaining lifespan of equipment so maintenance can be scheduled at the optimal time.

This project focuses on predicting the Remaining Useful Life (RUL) of aircraft engines using historical sensor measurements.

---

## 📂 Dataset

- **Dataset:** NASA CMAPSS Turbofan Engine Degradation Dataset
- **Subset Used:** FD001
- **Target Variable:** Remaining Useful Life (RUL)

The dataset contains:

- Engine ID
- Cycle Number
- Operational Settings
- Multiple Sensor Measurements

---

## 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Joblib
- Jupyter Notebook

---

## 🔄 Machine Learning Workflow

1. Data Loading
2. Exploratory Data Analysis (EDA)
3. Data Preprocessing
4. Feature Engineering (Remaining Useful Life)
5. Train-Test Split
6. Random Forest Regression
7. Model Evaluation
8. Feature Importance Analysis
9. Feature Selection
10. Manual Hyperparameter Tuning
11. GridSearchCV
12. Save Final Model

---

## 📊 Model Performance

### Baseline Random Forest

| Metric | Score |
|---------|-------|
| MAE | 25.4504 |
| RMSE | 35.9344 |
| R² | 0.7174 |

---

### Final Model

Hyperparameters:

- n_estimators = 200
- max_depth = 10

| Metric | Score |
|---------|-------|
| MAE | 25.2508 |
| RMSE | 35.5902 |
| R² | 0.7228 |

---

## 🔍 Feature Importance

Feature importance analysis was performed using the trained Random Forest model to identify the most influential variables.

Important observations:

- Engine cycle was the most significant predictor.
- Sensor 11 contributed strongly to prediction accuracy.
- Several low-importance sensors were removed and evaluated.
- Feature selection slightly reduced model performance, demonstrating that even low-importance features can collectively improve predictions.

---

## ⚙ Hyperparameter Tuning

Manual tuning experiments were performed by adjusting:

- Number of Trees (`n_estimators`)
- Maximum Tree Depth (`max_depth`)

GridSearchCV with **5-Fold Cross Validation** was then used to automatically search for the optimal hyperparameter combination.

---

## 💾 Model Deployment

The final trained model was saved using **Joblib**.

```python
joblib.dump(best_model, "predictive_maintenance_rf.pkl")
```

The saved model can later be loaded without retraining.

---

## 📁 Project Structure

```
NASA_Predictive_Maintenance/
│
├── Data/
├── Models/
│   └── predictive_maintenance_rf.pkl
├── Notebooks/
│   └── 01_NASA_Predictive_Maintenance.ipynb
├── Results/
├── README.md
└── requirements.txt
```

---

## 🚀 Future Improvements

- XGBoost Regression
- LightGBM
- LSTM for time-series prediction
- Streamlit Web Application
- Real-time predictive maintenance dashboard

---

## 👨‍💻 Author

**Vyshnav P S**

B.Tech Artificial Intelligence

Machine Learning | Predictive Analytics | AI Engineer
