# Ensemble Learning – ML Lab

This repository contains the implementation of five ensemble learning
scenarios as part of the Machine Learning lab. Each scenario covers a
different ensemble technique applied on different datasets.

---

## Libraries Used

- **pandas** – for loading and manipulating the datasets
- **numpy** – for numerical operations
- **matplotlib** – for plotting graphs and visualizations
- **scikit-learn** – for all machine learning models and metrics
- **imbalanced-learn** – for applying SMOTE in scenario 5

---

## Scenarios and Implementation

### Scenario 1 – Bagging
The dataset used is the Diabetes dataset where the goal is to predict
whether a patient has diabetes or not. A single Decision Tree was first
trained as a baseline model. Then BaggingClassifier was applied with 50
estimators, where each tree was trained on a random 80% subset of the
data and features. The accuracy of both models was compared using a bar
graph and a confusion matrix was plotted for the bagging model.

### Scenario 2 – Boosting
The dataset used is the Telco Customer Churn dataset where the goal is
to predict whether a customer will churn. Two boosting algorithms were
implemented – AdaBoost and Gradient Boosting. Categorical columns like
ContractType and InternetService were encoded using LabelEncoder before
training. ROC curves were plotted for both models and feature importance
was extracted and visualized from both AdaBoost and Gradient Boosting
separately.

### Scenario 3 – Random Forest
The dataset used is the Adult Income dataset where the goal is to
predict whether a person earns more than 50K or not. A Random Forest
model was trained and the number of trees was tuned by testing values
from 10 to 200. Accuracy was recorded for each value and plotted as a
graph. Feature importance was also extracted to understand which
features contributed the most to the prediction.

### Scenario 4 – Stacking
The dataset used is the Heart Disease dataset where the goal is to
predict the presence of heart disease. Three base models were trained –
Logistic Regression, SVM, and Decision Tree. These were then combined
using a StackingClassifier with Logistic Regression as the meta-learner.
The accuracy of all individual models and the stacked model were
compared using a bar chart.

### Scenario 5 – SMOTE
The dataset used is the Credit Card Fraud dataset where the goal is to
detect fraudulent transactions. The dataset had a heavy class imbalance
with only 8.3% fraud samples. A Random Forest model was first trained
on the imbalanced data. Then SMOTE was applied to balance the training
set and the model was retrained. Class distributions before and after
SMOTE were plotted, confusion matrices for both models were compared,
and a Precision-Recall curve was plotted to evaluate the improvement.

---

*Abhishek J – 24BAD002*  
*Kumaraguru College of Technology – AI & DS*
