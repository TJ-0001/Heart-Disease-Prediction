# Heart Disease Prediction

## Objective
The goal of this project is to **predict whether a person is at risk of heart disease** using the **Heart Disease UCI dataset**. This is a **binary classification problem**, where `0` indicates no heart disease and `1` indicates the presence of heart disease.

---

## Dataset
- **Name:** Heart Disease UCI Dataset  
- **Source:** [Kaggle](https://www.kaggle.com/ronitf/heart-disease-uci)  
- **Features (16 columns):**  
  - `age` – Age of the patient  
  - `sex` – Gender  
  - `cp` – Chest pain type  
  - `trestbps` – Resting blood pressure  
  - `chol` – Serum cholesterol  
  - `fbs` – Fasting blood sugar > 120 mg/dl  
  - `restecg` – Resting ECG results  
  - `thalch` – Maximum heart rate achieved  
  - `exang` – Exercise-induced angina  
  - `oldpeak` – ST depression induced by exercise  
  - `slope` – Slope of the ST segment  
  - `ca` – Number of major vessels colored  
  - `thal` – Thalassemia (normal, fixed, reversible)  
  - `num` – Original target (converted to binary `target`)  
- **Size:** 920 records  

---

## Models Applied
1. **Logistic Regression**  
   - Provides probabilities and coefficients to understand feature influence.  
2. **Decision Tree Classifier**  
   - Captures non-linear relationships and identifies important features.  

---

## Key Results

### Model Performance
| Model | Accuracy | ROC-AUC |
|-------|---------|---------|
| Logistic Regression | ~82% | ~89% |
| Decision Tree | ~77% | ~82% |

### Confusion Matrices
- Both models were evaluated using confusion matrices and ROC curves.

---

## Feature Importance

### Logistic Regression (Coefficient Signs)
- **Positive:** `cp`, `oldpeak`, `exang`, `age` → increase heart disease risk  
- **Negative:** `thalch`, `chol` → decrease risk  

### Decision Tree
| Feature | Importance |
|---------|------------|
| cp (chest pain) | 0.46 |
| chol | 0.18 |
| age | 0.10 |
| oldpeak | 0.09 |
| thalch | 0.07 |
| sex | 0.05 |
| exang | 0.03 |

**Interpretation:**  
- Chest pain type (`cp`) is the strongest predictor.  
- Exercise-related features (`oldpeak`, `thalch`, `exang`) and age also influence risk.  

---

## Insights & Conclusions
1. **Chest pain type** and **ST depression** are key indicators of heart disease.  
2. Logistic Regression shows **direction of effect** (which features increase/decrease risk).  
3. Decision Tree highlights **features most frequently used for splits**.  
4. Models align with **clinical knowledge** about cardiovascular risk factors.  
5. The analysis can help in **early identification of high-risk patients**.  

---

## Files Included
- **heart_disease_prediction.ipynb** — Jupyter Notebook containing all code, visualizations, and outputs.
- **heart_disease_uci.csv** — Dataset used for analysis and visual exploration.
---

## 🔗 References
- Heart Disease UCI Dataset: [Kaggle link](https://www.kaggle.com/datasets/redwankarimsony/heart-disease-data)  
