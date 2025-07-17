
# 🧠 Predicting Metal Ion Concentration from Multi-Parameter Water Samples using KNN Regression and Cross-Validation

This project focuses on evaluating the predictive capability of **K-Nearest Neighbors Regression (KNNR)** for estimating metal ion concentrations—specifically `c_total`, `Cd`, and `Pb`—from sensor-modulated features (`Mod1`, `Mod2`, `Mod3`) using a dataset of 225 water samples. The model performance is assessed using **two cross-validation strategies**:  
- **Leave-One-Out Cross-Validation (LOOCV)**  
- **Leave-Replicas-Out Cross-Validation (LROCV)**  
The evaluation metric used is **C-Index**, implemented via Somers’ D correlation.

---

## 📊 Dataset

- **File:** `water_data.csv`  
- **Size:** 225 samples × 6 columns  
- **Features:** `Mod1`, `Mod2`, `Mod3`  
- **Targets:** `c_total`, `Cd`, `Pb`  
- The data includes 129 mixtures with 3 replicas and 96 mixtures with 4 replicas.

---

## 🔍 Tasks Performed

- Implemented KNN regression using `k = [1, 3, 5, 7]`
- Applied both **LOOCV** and **LROCV** techniques
- Evaluated model using **C-index** for all 3 target variables
- Visualized comparative performance between CV methods

---

## 📈 Results (C-Index)

**LOOCV:**  
| k | c_total | Cd     | Pb     |
|---|---------|--------|--------|
| 1 | 0.908   | 0.922  | 0.881  |
| 3 | 0.914   | 0.900  | 0.874  |
| 5 | 0.894   | 0.862  | 0.854  |
| 7 | 0.874   | 0.814  | 0.836  |

**LROCV:**  
| k | c_total | Cd     | Pb     |
|---|---------|--------|--------|
| 1 | 0.818   | 0.778  | 0.738  |
| 3 | 0.819   | 0.761  | 0.769  |
| 5 | 0.812   | 0.740  | 0.748  |
| 7 | 0.816   | 0.715  | 0.762  |

---

## 💡 Key Reflections

- **LOOCV** gave more optimistic estimates due to similarity between test and training data.
- **LROCV** provided a **more realistic** estimate of generalization performance since all replicas of a test mixture were excluded from training.
- C-index values dropped in LROCV, highlighting the importance of **independence in evaluation**.

---

## 🛠️ Skills Used

- Python (`pandas`, `scikit-learn`, `matplotlib`)
- K-Nearest Neighbor Regression
- Leave-One-Out & Leave-Replicas-Out Cross-Validation
- Statistical validation with Somers’ D correlation (C-Index)

