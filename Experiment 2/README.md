This folder contains two Jupyter notebooks for Experiment 2:

- `Experiment 2/EXP-2-Scenario-1.ipynb` — regression analysis predicting air temperature (`Dry_T`) from oceanographic features.
  - Notebook: [Experiment 2/EXP-2-Scenario-1.ipynb](https://github.com/j-abhishek26/24ADI003---24BAD002/blob/main/Experiment%202/EXP-2-Scenario-1.ipynb)

- `Experiment 2/EXP-2-Scenario-2.ipynb` — binary classification to predict daily price movement (Close > Open) for a stock dataset.
  - Notebook: [Experiment 2/EXP-2-Scenario-2.ipynb](https://github.com/j-abhishek26/24ADI003---24BAD002/blob/main/Experiment%202/EXP-2-Scenario-2.ipynb)

Each notebook is runnable in Google Colab or a local Jupyter environment. They include data loading (via `kagglehub`), preprocessing, model training, evaluation and visualization.

---

## Notebook summaries

### EXP-2-Scenario-1.ipynb (Regression)
- Goal: Predict `Dry_T` (air temperature) using three features:
  - `Lat_Dec`, `Lon_Dec`, `Bottom_D`
- Dataset: `sohier/calcofi` — `cast.csv` (loaded via `kagglehub.dataset_load`)
- Preprocessing:
  - Select features + target
  - Impute missing values with column means (`SimpleImputer(strategy='mean')`)
  - Standard scaling of features (`StandardScaler`)
  - Train/test split (test_size=0.2, random_state=42)
- Models trained:
  - Linear Regression
  - Ridge (alpha=1.0)
  - Lasso (alpha=0.01)
- Key evaluation results (from the notebook):
  - Linear Regression:
    - MSE: 3.6748014404014953
    - RMSE: 1.916977162201338
    - R²: 0.08479369479916654
  - Ridge R²: 0.08479390371327222
  - Lasso R²: 0.08468909730175578
- Visualizations included:
  - Actual vs Predicted scatter with identity line
  - Residual distribution
  - Feature correlation heatmap
- Notes:
  - Low R² indicates the chosen features explain little variance in `Dry_T`. Consider adding more predictors and feature engineering.

### EXP-2-Scenario-2.ipynb (Classification)
- Goal: Predict whether the stock price moved up that day (`Price_Movement` = Close > Open) using `Open`, `High`, `Low`.
- Dataset: `debashis74017/lic-stock-price-data` — file: `LICI - Daily data.csv` (loaded via `kagglehub.dataset_load`)
- Preprocessing:
  - Create binary target `Price_Movement = (Close > Open).astype(int)`
  - Forward-fill missing values (`df.ffill(inplace=True)`)
  - Standard scale features
  - Train/test split with stratification (test_size=0.2, random_state=42)
- Model:
  - LogisticRegression(max_iter=1000)
- Key evaluation results (from the notebook):
  - Accuracy: 0.70
  - Precision: 0.00
  - Recall: 0.00
  - F1 Score: 0.00
  - Classification report shows class imbalance (support: 14 for class 0, 6 for class 1)
  - Feature coefficients printed (sorted):
    - High: 0.996090
    - Low: 0.309411
    - Open: -1.254235
- Visualizations included:
  - Confusion matrix heatmap
  - ROC curve (AUC computed in notebook)
  - Barplot of feature coefficients
- Notes:
  - Precision/recall of 0 indicates the classifier predicted only the majority class. Use class-balancing strategies (resampling, class weights) or try other features/models.

---
