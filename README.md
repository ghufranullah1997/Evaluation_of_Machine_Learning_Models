# 📊 Evaluation of Machine Learning Methods

This repository contains material and summaries related to the course **"Evaluation of Machine Learning Methods"**, which builds on the foundation laid by *Data Analysis and Knowledge Discovery* and *Statistical Data Analysis*. The course emphasizes statistical techniques for estimating the real-world performance of AI and machine learning systems.

---

## 🎯 Learning Outcomes

I am able to:

- Understand the theoretical underpinnings of prediction performance estimation
- Identify when standard assumptions (e.g., IID, Law of Large Numbers) break down
- Apply hold-out, cross-validation, and nested CV techniques in both model evaluation and model selection
- Design task-specific resampling strategies tailored for complex real-world settings
- Evaluate model trustworthiness for cases where training and new data distributions differ in a known way
- Implement custom evaluation setups for domain-specific challenges in:
  - Chemoinformatics
  - Medical informatics
  - Geoinformatics
  - Bioinformatics and recommender systems

---

## 📚 Course Content Overview

The course introduced both classical and modern concepts in evaluation theory and linked them with applied machine learning:

### 🧠 Theoretical Foundation
- Prediction performance estimation theory
- IID assumption and its limitations
- Law of Large Numbers and estimator generalization

### 🛠 Practical Resampling Techniques
- Hold-out, k-fold cross-validation, leave-one-out CV
- Nested cross-validation for model selection and evaluation
- Group- and subject-level CV (e.g., leave-one-patient-out)
- Spatial CV for geospatial data (distance-aware folds)
- Cold-start CV for pairwise prediction problems (e.g., drug–target, user–item)

### 🔬 Domain-Specific Evaluation Design
- Estimating generalization across unseen patients or populations
- Distance-aware prediction in geoinformatics
- Predicting novel interaction pairs in recommender systems

---
