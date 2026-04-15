# 📊 Experiment 7: Clustering using K-Means & GMM

This experiment focuses on **unsupervised learning**, where the goal is to group similar data points without predefined labels.

---

## 🔍 What is Clustering?

Clustering is used to divide data into groups (clusters) such that:
- Points in the same cluster are similar
- Points in different clusters are dissimilar

---

## ⚙️ Algorithms Used

### 1. K-Means Clustering
- Divides data into **K clusters**
- Each cluster has a **centroid (mean point)**
- Data points are assigned to the nearest centroid

#### Working:
1. Choose number of clusters (K)
2. Initialize centroids randomly
3. Assign points to nearest centroid
4. Update centroids based on assigned points
5. Repeat until convergence

---

### 2. Gaussian Mixture Model (GMM)
- A **probabilistic clustering method**
- Assumes data is generated from multiple Gaussian distributions

#### Key Idea:
- Instead of hard assignment (like K-Means),
  GMM gives **probability of belonging to each cluster**

#### Working:
1. Initialize parameters (mean, covariance)
2. Expectation step → assign probabilities
3. Maximization step → update parameters
4. Repeat until stable

---

## 🧪 What This Code Does

- Loads dataset
- Applies **K-Means clustering**
- Applies **GMM clustering**
- Visualizes clusters using graphs
- Compares how both methods group data

---

## 📊 Output

- Clustered data points plotted visually
- Comparison between:
  - Hard clustering (K-Means)
  - Soft clustering (GMM)

---

## 🧠 Key Learning

- Difference between **distance-based** and **probabilistic** clustering
- Understanding how cluster boundaries change
- Visualization of unsupervised learning

---

## 📌 Conclusion

K-Means is simple and fast, but GMM is more flexible as it considers data distribution.

