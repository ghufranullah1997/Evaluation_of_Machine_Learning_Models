
# Spatial KNN Regression for Water Permeability Prediction

This project addresses the evaluation of spatial prediction performance using the **7-Nearest Neighbors (7NN)** regression model to estimate water permeability in forestry based on geographic distance.

## 📁 Dataset Overview

- **input.csv**: 1690 samples × 75 predictor features
- **output.csv**: 1690 water permeability target values
- **coordinates.csv**: 1690 corresponding 2D spatial coordinates (in meters)

## 🧠 Objective

Estimate how spatial distance impacts the performance of a 7NN regression model using spatial leave-one-out cross-validation and report the model’s performance using the **C-index** as the metric.

## 🔧 Methods

- **Preprocessing**: Z-score standardization of all 75 input features.
- **Cross-Validation**: Spatial Leave-One-Out CV (SLOO-CV) using 7NN, repeated for distance thresholds: 0, 20, 40, ..., 300 meters.
- **Evaluation Metric**: C-index computed per threshold.
- **Distance Computation**: Euclidean distance matrix computed between all coordinate pairs.

## 📊 Key Findings

- C-index decreases as the spatial distance between train and test increases.
- Performance remains **≥ 0.68 up to ~100 meters**, after which accuracy declines.
- Beyond **140 meters**, the performance stabilizes at ~0.586, suggesting weaker spatial correlation.

## 📈 Visualization

Two main plots were produced:

- **C-index vs. Distance Threshold Line Chart**
- **C-index vs. Distance Threshold Bar Chart**

These clearly show performance drop-off beyond 100 meters.

## 💡 Reflections

- Predictions are most reliable within **100m** proximity.
- Results validate the **spatial autocorrelation** assumption: closer observations yield better predictions.
- Spatial KNN models must consider distance constraints to ensure predictive trustworthiness.

---
## You can access the full project here:
- 📄 [Jupyter Notebook][(https://github.com/ghufranullah1997/Evaluation_of_Machine_Learning_Models/blob/main/Project/Project%202/EMLM2025_exercise2.ipynb)]




