# 🔹 Experiment 4 – Naive Bayes Classification

## 🎯 Objective
To implement and analyze Naive Bayes classifiers on both text and numerical datasets.

---

## 📌 Scenario 1 – SMS Spam Detection (Multinomial Naive Bayes)

### 🔍 Dataset
SMS Spam Collection Dataset

### ⚙️ Implementation Steps
- Extracted dataset from ZIP
- Cleaned text using regex (lowercase + remove special characters)
- Converted text to numerical form using `CountVectorizer`
- Encoded labels using `LabelEncoder`
- Split into training and testing sets
- Trained **Multinomial Naive Bayes**
- Evaluated using Accuracy, Precision, Recall, F1 Score
- Plotted Confusion Matrix
- Extracted top spam-influencing words

###  Key Learning
- Multinomial NB works well for text classification.
- Word frequency plays a major role in spam detection.

---

##  Scenario 2 – Iris Dataset (Gaussian Naive Bayes)

###  Dataset
Iris Dataset (from sklearn)

###  Implementation Steps
- Loaded dataset using `load_iris()`
- Standardized features using `StandardScaler`
- Split into train and test sets
- Trained **Gaussian Naive Bayes**
- Evaluated using classification metrics
- Compared with Logistic Regression
- Visualized Decision Boundary

###  Key Learning
- Gaussian NB assumes normal distribution.
- Works efficiently for small, clean datasets.

---

