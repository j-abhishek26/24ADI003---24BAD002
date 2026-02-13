# Experiment 3: Regression Analysis

## EXP-3-SCENARIO-1: Student Performance Prediction

**Objective:** Predict final exam scores based on student characteristics and study habits.

**Dataset:** StudentsPerformance.csv

**Features Used:**
- Study hours
- Attendance percentage
- Parental level of education
- Test preparation course completion
- Sleep hours

**Models Implemented:**
- Linear Regression
- Ridge Regression
- Lasso Regression

**Key Results:**
- Linear Regression R² Score: 0.0341
- RMSE: 14.39
- Ridge R² Score: 0.0342
- Lasso R² Score: 0.0343

**Feature Importance (by coefficient magnitude):**
1. Test preparation course: -3.85
2. Parental level of education: -1.01
3. Sleep hours: 0.86
4. Attendance: -0.40
5. Study hours: 0.23

**Visualizations:**
- Actual vs Predicted exam scores line plot
- Feature influence bar chart
- Residual distribution histogram

---

## EXP-3-SCENARIO-2: Polynomial Regression - MPG Prediction

**Objective:** Predict fuel efficiency (MPG) using polynomial regression with horsepower as the predictor.

**Dataset:** auto-mpg.csv

**Approach:** Polynomial feature transformation (degrees 2, 3, and 4) with StandardScaler normalization.

**Models Evaluated:**
- Polynomial Linear Regression (Degree 2, 3, 4)
- Ridge Regression

**Key Results:**
- Degree 2: R² = 0.7407, RMSE = 3.73
- Degree 3: R² = 0.7398, RMSE = 3.74
- Degree 4: R² = 0.7314, RMSE = 3.80
- Ridge R² Score: 0.7409

**Observations:**
- Degree 2 polynomial provides optimal balance
- Higher degrees show signs of overfitting
- Ridge regularization maintains performance

**Visualizations:**
- Polynomial curve fitting comparison
- Training vs Testing error by degree
- Underfitting vs Overfitting demonstration

---

**Author:** ABHISHEK J (24BAD002)
