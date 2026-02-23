#  Experiment 5 – KNN & Decision Tree

##  Objective
To implement distance-based and tree-based classification algorithms and analyze their behavior.

---

##  Scenario 1 – K-Nearest Neighbors (Breast Cancer Dataset)

###  Implementation Steps
- Loaded dataset from ZIP
- Handled missing values
- Applied `StandardScaler`
- Trained **KNN (k=5)**
- Evaluated using Accuracy and Confusion Matrix
- Tested different K values (1–20)
- Plotted Accuracy vs K graph
- Visualized Decision Boundary

###  Key Learning
- K vlue strongly affects accuracy.
- Feature scaling is essential for KNN.

---

##  Scenario 2 – Decision Tree (Loan Prediction Dataset)

###  Implementation Steps
- Loaded dataset
- Filled missing values using mode
- Encoded categorical variables
- Trained Decision Tree with controlled depth
- Evaluated model performance
- Plotted Feature Importance
- Visualized Tree Structure
- Performed Overfitting Analysis

###Key Learning
- Decision Trees are easy to interpret.
- Increasing depth may lead to overfitting.

---

#  Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn

---
