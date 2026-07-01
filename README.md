# ✈️ NASA Predictive Maintenance using Random Forest Regression

Predicting the **Remaining Useful Life (RUL)** of aircraft engines using the **NASA CMAPSS Turbofan Engine Degradation Dataset (FD001)** and **Random Forest Regression**.

---

# 📖 Project Overview

Predictive Maintenance uses historical sensor measurements to estimate how many operational cycles remain before an aircraft engine reaches failure.

This project develops a complete Machine Learning pipeline that predicts the **Remaining Useful Life (RUL)** of aircraft engines using the NASA CMAPSS dataset.

The project covers the complete ML workflow, including:

- Data Exploration
- Data Preprocessing
- Feature Engineering
- Random Forest Regression
- Feature Importance Analysis
- Feature Selection
- Hyperparameter Tuning
- GridSearchCV
- Model Evaluation

---

# 🎯 Objective

Build a Machine Learning model capable of predicting the Remaining Useful Life (RUL) of aircraft engines to support predictive maintenance and reduce unexpected failures.

---

# 📂 Dataset

**Dataset:** NASA CMAPSS Turbofan Engine Degradation Simulation Dataset

**Subset Used:** FD001

The dataset contains:

- Engine ID
- Cycle Number
- Operational Settings
- Sensor Measurements
- Remaining Useful Life (RUL)

> **Note:** The dataset is publicly available from NASA and is not included in this repository.

---

# 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Joblib
- Jupyter Notebook

---

# 🔄 Machine Learning Workflow

1. Import Libraries
2. Load Dataset
3. Exploratory Data Analysis (EDA)
4. Data Preprocessing
5. Feature Engineering (RUL)
6. Train-Test Split
7. Random Forest Regression
8. Model Evaluation
9. Feature Importance Analysis
10. Feature Selection
11. Manual Hyperparameter Tuning
12. GridSearchCV
13. Save Final Model

---

# 📊 Model Performance

## Baseline Random Forest

| Metric | Score |
|---------|-------:|
| MAE | 25.4504 |
| RMSE | 35.9344 |
| R² | 0.7174 |

---

## Final Selected Model

Although GridSearchCV selected **300 trees** with **max_depth = 10**, evaluation on the unseen test dataset showed that the manually tuned model performed slightly better.

### Final Hyperparameters

- Random Forest Regressor
- n_estimators = **200**
- max_depth = **10**
- random_state = **42**

### Final Performance

| Metric | Score |
|---------|-------:|
| MAE | **25.2508** |
| RMSE | **35.5902** |
| R² | **0.7228** |

---

# 📈 Feature Importance

Feature importance analysis showed that:

- Engine cycle was the most influential feature.
- Sensor 11 contributed significantly to prediction accuracy.
- Low-importance sensors were evaluated through feature selection experiments.
- Removing low-importance features did not improve overall model performance.

The complete feature importance visualization is available in the **Results** folder.

---

# ⚙ Hyperparameter Tuning

The model was improved through two stages:

### Manual Hyperparameter Tuning

- Increased the number of trees
- Controlled tree depth
- Compared multiple Random Forest models

### Automated Hyperparameter Tuning

GridSearchCV with **5-Fold Cross Validation** was used to evaluate multiple hyperparameter combinations automatically.

---

# 📁 Repository Structure

```
NASA-Predictive-Maintenance
│
├── Notebooks/
│   └── NASA_Predictive_Maintenance_Random_Forest.ipynb
│
├── Results/
│   ├── feature_importance.png
│   ├── model_comparison.csv
│   └── final_metrics.txt
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

# 📄 Results

The Results folder contains:

- Feature Importance Plot
- Model Comparison Table
- Final Evaluation Metrics

---

# 🚀 Future Improvements

- XGBoost Regression
- LightGBM
- LSTM-based Remaining Useful Life Prediction
- Streamlit Deployment
- Real-time Predictive Maintenance Dashboard

---

# 👨‍💻 Author

**Vyshnav P S**

B.Tech in Artificial Intelligence

Interested in:
- Machine Learning
- Artificial Intelligence
- Predictive Analytics
- Aviation AI
