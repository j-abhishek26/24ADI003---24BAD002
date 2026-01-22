# 24BAD002 - ABHISHEK J
# Data Analysis Scenarios

This repository contains four Jupyter notebooks that demonstrate exploratory data analysis (EDA) and basic visualization workflows on different datasets. Each notebook is self-contained and shows typical first steps for understanding a dataset (loading, summary statistics, missing-value checks, simple plots), plus notes & suggestions for next steps.

## Notebooks

### SCENARIO-1.ipynb
- Dataset: `carrie1/ecommerce-data` (loaded from `/kaggle/input/ecommerce-data/data.csv`)
- Purpose: Exploratory analysis of online retail transactions.
- Key steps:
  - Load CSV (encoding ISO-8859-1).
  - Inspect head/tail, `info()`, `describe()`.
  - Check missing values (`CustomerID` has many nulls).
  - Aggregate `Quantity` by `Description` to find top-selling products.
  - Simple bar and line plots for top products.
- Notes / suggestions:
  - Large dataset (~541,909 rows) — expect memory/time cost for heavy ops.
  - There are obvious data issues / outliers (negative quantities, negative unit prices) and possible cancelled orders. Consider:
    - Converting `InvoiceDate` to datetime.
    - Removing cancellations or returned items (e.g., negative quantities or invoices starting with 'C').
    - Creating `Revenue = Quantity * UnitPrice`.
    - Filling or removing missing `CustomerID` depending on analysis needs.

### SCENARIO-2.ipynb
- Dataset: `uciml/pima-indians-diabetes-database` (loaded from `/kaggle/input/pima-indians-diabetes-database/diabetes.csv`)
- Purpose: Basic EDA on diabetes diagnostic dataset.
- Key steps:
  - Load dataset and display `head()`.
  - Run `info()` and `describe()` to examine types and distributions.
  - Plot histogram of `Glucose` and boxplot for `Age`.
- Notes / suggestions:
  - Dataset size: 768 rows.
  - Some columns use zero values to indicate missing measurements (e.g., `Glucose`, `BloodPressure`, `SkinThickness`, `Insulin`, `BMI`). Treat zeros appropriately (replace with NaN and impute or remove) before modeling.
  - Next steps: feature scaling, train/test split, classification models (logistic regression / tree-based models), cross-validation, and evaluation (ROC/AUC, confusion matrix).

### SCENARIO-3.ipynb
- Dataset: `Housing.csv` (local file in repo / expected to be in working directory)
- Purpose: House-price exploratory analysis and relationships between numeric features.
- Key steps:
  - Load CSV and show `head()`.
  - Show columns and numeric `describe()`.
  - Check for missing values (none reported).
  - Scatter plot `area` vs `price` and a numeric correlation heatmap.
- Notes / suggestions:
  - Medium-sized (~545 rows).
  - Contains both numeric features (area, bedrooms, bathrooms, parking, etc.) and categorical fields (furnishing status, mainroad, etc.) — need encoding for modeling.
  - Next steps: clean/encode categorical variables, engineer features (price per sqft, age, etc.), and build regression models (linear regression, tree ensembles).

### SCENARIO-4.ipynb
- Dataset: `imakash3011/customer-personality-analysis` (marketing_campaign.csv, loaded with tab separator)
- Purpose: Customer behavior / marketing campaign exploratory analysis.
- Key steps:
  - Load dataset and display `head()`, `info()`, `describe()`.
  - Check missing values (e.g., `Income` has some missing entries).
  - Basic EDA and summary statistics for many purchase- and interaction-related features.
- Notes / suggestions:
  - Dataset size: 2,240 rows and 29 columns (mixture of numeric and categorical).
  - Useful derived features: total money spent, average spend per product category, tenure (from `Dt_Customer`), and purchase frequency.
  - Target examples: predict `Response` to campaigns (classification) or perform customer segmentation (clustering).
  - Watch for outliers in `Income` and skewed spend variables; parse dates and impute missing income values appropriately.

## How to run
1. Install required packages:
   - Python 3.x, pandas, numpy, matplotlib (and optionally scikit-learn for modeling).
   - Notebooks use `kagglehub` in some cells to fetch datasets (works in Colab with kagglehub support). Alternatively, download datasets manually via Kaggle and place them under `/kaggle/input/` or update the file paths in notebooks.
2. Open each notebook in Jupyter, Colab, or Kaggle Notebooks and run cells in order.
3. For modeling or deeper analysis, follow the "Notes / suggestions" in each notebook.

## Dependencies
- pandas, numpy, matplotlib
- Optional: kagglehub or Kaggle API (for dataset download), scikit-learn (for modeling)

## Contact
If you want improvements, additional cleaning/modeling steps, or converted .py scripts, open an issue or contact the repository owner.
