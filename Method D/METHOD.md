
## 📊 Workflow Summary

### 1. Exploratory Data Analysis (EDA)
- Overview of data shape, types, and descriptive statistics
- Visualization and summary of missing values

### 2. Data Preprocessing
- **Missing Value Handling**:
  - Numerical: Imputed using mean
  - Categorical: Imputed using mode
- **Encoding**:
  - Ordinal encoding for categorical features using `OrdinalEncoder`
  - One-hot encoding applied later in the preprocessing pipeline using `ColumnTransformer`
- **Feature Scaling**:
  - Standardization using `StandardScaler`

### 3. Feature Engineering

Custom feature transformations were applied to enhance model performance. After processing:

- Original training data shape: `(61609, 62)`
- Original test data shape: `(41074, 61)`
- After feature engineering: **73 features**
- Training split: `(49287, 73)` | Validation split: `(12322, 73)`

```python
# Apply feature engineering
features_processed = feature_engineering(features)
test_features_processed = feature_engineering(test_features)

# Ensure both datasets have the same columns
common_columns = sorted(list(set(features_processed.columns) & set(test_features_processed.columns)))
features_final = features_processed[common_columns]
test_features_final = test_features_processed[common_columns]
```

---

## 🏗️ Model Training

Models evaluated:

- Linear Regression
- Ridge & Lasso Regression
- Decision Tree Regressor
- Random Forest Regressor
- Extra Trees Regressor
- Gradient Boosting Regressor
- K-Nearest Neighbors Regressor
- XGBoost
- LightGBM
- CatBoost

Each model was trained and validated using RMSE, MAE, R², and training time.

---

## 🏆 Model Performance Summary

Sorted by RMSE (lower is better):

| Model Name            | RMSE     | R²       | MAE     | Training Time (s) |
|-----------------------|----------|----------|---------|-------------------|
| Extra Trees           | 11.24    | 0.7287   | 6.71    | 201.54            |
| CatBoost              | 13.04    | 0.6351   | 9.27    | 15.24             |
| Random Forest         | 13.46    | 0.6112   | 9.68    | 362.59            |
| XGBoost               | 14.45    | 0.5516   | 10.95   | 3.84              |
| LightGBM              | 14.94    | 0.5210   | 11.45   | 3.15              |
| K-Nearest Neighbors   | 15.54    | 0.4816   | 8.22    | 3.12              |
| Decision Tree         | 16.58    | 0.4096   | 8.72    | 4.18              |
| Gradient Boosting     | 17.15    | 0.3683   | 13.65   | 79.38             |
| Ridge Regression      | 19.37    | 0.1948   | 15.63   | 0.70              |
| Linear Regression     | 19.37    | 0.1944   | 15.63   | 0.95              |
| Lasso Regression      | 20.12    | 0.1311   | 16.53   | 0.70              |

📌 **Best Model: Extra Trees Regressor** with RMSE = **11.24**, R² = **0.7287**

---

## 📈 Evaluation Metrics

| Metric | Description |
|--------|-------------|
| RMSE   | Penalizes larger errors more than smaller ones |
| MAE    | Measures average magnitude of errors |
| R²     | Indicates goodness-of-fit (higher is better) |

---

## 🚀 How to Run

### Prerequisites

Install the required packages:
```bash
pip install numpy pandas scikit-learn xgboost lightgbm catboost
```

### Running Instructions

1. Clone the repository or upload the notebook to Jupyter/Colab.
2. Ensure `train.csv` and `test.csv` are available in the correct path.
3. Run each cell sequentially to:
   - Load and preprocess data
   - Apply feature engineering
   - Train and evaluate models
   - Predict on the test set

---

## 📁 Output

- Cleaned and processed datasets
- Evaluation metrics for all models
- Final predictions for the test set (as CSV)

---

## 🧠 About

This notebook was developed as part of the **MLx 2.0** regression competition to demonstrate practical applications of machine learning on structured data, including feature engineering, model comparison, and performance evaluation.
