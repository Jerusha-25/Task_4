# Task 4: Classification with Logistic Regression

## 🧠 Objective
Build a binary classifier using **Logistic Regression** to predict whether a tumor is **Malignant (M)** or **Benign (B)** based on breast cancer diagnostic data.

---

## 🔧 Tools & Libraries Used
- [Scikit-learn](https://scikit-learn.org/)
- [Pandas](https://pandas.pydata.org/)
- [Matplotlib](https://matplotlib.org/)
- [NumPy](https://numpy.org/)

---

## 📂 Dataset
- **Source**: [Breast Cancer Wisconsin (Diagnostic) Data Set](https://archive.ics.uci.edu/ml/datasets/breast+cancer+wisconsin+(diagnostic))
- **Attributes**: 30 numerical features + diagnosis label (`M` = Malignant, `B` = Benign)

---

## 📌 Project Steps

1. **Load & Clean the Data**
   - Removed irrelevant columns (`id`, `Unnamed: 32`)
   - Converted diagnosis labels to binary (M = 1, B = 0)
   - Handled missing values using `SimpleImputer`

2. **Feature Scaling**
   - Standardized features using `StandardScaler` to improve model convergence.

3. **Train-Test Split**
   - Used 80% of data for training and 20% for testing.

4. **Model Training**
   - Trained a **Logistic Regression** model with high `max_iter` to ensure convergence.

5. **Evaluation Metrics**
   - Accuracy
   - Precision
   - Recall
   - Confusion Matrix
   - ROC-AUC Score
   - ROC Curve

6. **Threshold Tuning**
   - Evaluated model performance using different classification thresholds (0.3, 0.5, 0.7)
   - Discussed trade-offs between **precision** and **recall**

7. **Visualization**
   - ROC Curve
   - 2D decision boundary (sigmoid surface projection)
   - Sigmoid function plot with visible points

---

## 📊 Results Summary

| Threshold | Accuracy | Precision | Recall | ROC-AUC |
|-----------|----------|-----------|--------|---------|
| 0.3       | 95.61%   | 91.30%    | 97.67% | 0.96    |
| 0.5       | 97.37%   | 97.62%    | 95.35% | 0.97    |
| 0.7       | 98.25%   | 100.00%   | 95.35% | 0.98    |

---

## 📈 Sigmoid Function

A sigmoid curve was plotted to demonstrate the probability mapping of the logistic function:

\[
\sigma(z) = \frac{1}{1 + e^{-z}}
\]

Markers were added for visual clarity.

---

## ✅ Conclusion

This project demonstrates how logistic regression can be effectively used for binary classification tasks such as cancer detection. By adjusting classification thresholds, we can control for different business or health-related requirements, balancing between **false positives** and **false negatives**.

---

