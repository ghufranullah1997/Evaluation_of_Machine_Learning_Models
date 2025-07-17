
# 📘 Drug-Target Binding Affinity Estimation using Cross-Validation Techniques

This project addresses a common pitfall in evaluating machine learning models on *pair-input* datasets, particularly in drug discovery research involving **protein-drug binding affinity prediction**. The objective was to diagnose and correct a flawed cross-validation approach that resulted in misleading model performance and to develop a robust evaluation pipeline using proper cross-validation strategies.

---

## 📌 Project Overview

- **Objective**: Assess and correct the cross-validation strategy used to estimate the generalization performance of a K-Nearest Neighbors (KNN) model trained on 400 protein-drug affinity measurements.
- **Problem**: The original Leave-One-Out Cross-Validation (LOOCV) led to **over-optimistic scores (C-Index > 90%)** due to data leakage, where the same proteins and drugs appeared in both training and test sets.
- **Fix**:
  - Implemented **Leave-Pair-Out CV** and **Grouped K-Fold CV** to ensure no overlap between training and test sets.
  - Evaluated using **Pearson correlation** and **C-Index** for reliability.

---

## 📊 Results

- **Leave-Pair-Out Cross-Validation**:
  - Pearson Correlation: **0.868**
  - C-Index: **0.830**
- **Grouped K-Fold Cross-Validation (5-fold, grouped by proteins)**:
  - Pearson Correlation: **0.810**
  - C-Index: **0.794**

These values reflect a **more realistic** performance estimate of the model in predicting affinities for unseen protein-drug pairs.

---

## 🧠 Key Takeaways

- Highlighted how improper cross-validation (like vanilla LOOCV) on pair-input data causes data leakage and overestimates performance.
- Introduced **custom LPO** and **group-aware CV** strategies for valid estimation.
- Emphasized the need for **domain-aware validation schemes** in real-world biological ML problems.

---

## 🛠️ Technologies & Skills

- **Python**, **NumPy**, **Pandas**, **scikit-learn**
- Model: **KNeighborsRegressor**
- Evaluation metrics: **Pearson correlation**, **Concordance Index (C-index)**
- Techniques: **Leave-Pair-Out CV**, **GroupKFold CV**, **cross-validation in pairwise data**

---

## You can view the project:
[🔗 View Project Notebook](https://github.com/ghufranullah1997/Evaluation_of_Machine_Learning_Models/blob/main/Project/Project%203/exercise-3-final-draft.ipynb)

