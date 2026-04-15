# 🎯 Experiment 10: Recommendation System using SVD & NMF

This experiment focuses on building a **recommendation system** using matrix factorization techniques.

---

## 🔍 What is a Recommendation System?

A recommendation system suggests items (movies, products, etc.) to users based on:
- Their past behavior
- Similar users or items

---

## ⚙️ Techniques Used

### 1. SVD (Singular Value Decomposition)

- Decomposes the user-item matrix into 3 matrices
- Helps in identifying **hidden patterns (latent factors)**

#### Idea:
- Users and items are represented in a lower-dimensional space
- Missing ratings are predicted using these factors

---

### 2. NMF (Non-negative Matrix Factorization)

- Similar to SVD but all values are **non-negative**
- More interpretable for recommendation systems

#### Idea:
- Breaks matrix into:
  - User features
  - Item features
- Combines them to predict ratings

---

## 🧪 What This Code Does

- Loads user-item interaction data
- Converts data into matrix form
- Applies:
  - SVD model
  - NMF model
- Predicts missing ratings
- Recommends items to users

---

## 📊 Output

- Predicted ratings for unseen items
- Top recommended items for each user

---

## 🧠 Key Learning

- Understanding **matrix factorization**
- How recommendation systems work internally
- Difference between SVD and NMF

---

## 📌 Conclusion

Both SVD and NMF help in generating recommendations by learning hidden patterns:
- SVD is more general
- NMF is easier to interpret

---

## 🚀 Use Case

- Movie recommendation (Netflix)
- Product recommendation (Amazon)
- Music recommendation (Spotify)

