# 🩺 Heart Disease Risk Prediction (CS439 Final Project)

This machine learning project aims to **predict the presence of heart disease** using the **Cleveland Heart Disease dataset**. It explores the impact of data preprocessing, model selection, hyperparameter tuning, and interpretability methods to build a clinically-relevant and trustworthy diagnostic model.

### 👨‍🔬 Collaborators
- **Itay Akad**
- **Ron Cohen**
- **Itay Weinberg**

---

## 📁 Project Overview

We implemented and evaluated multiple classification models to identify individuals at risk of heart disease. The final pipeline includes:

- Logistic Regression (baseline)
- Decision Tree Classifier
- Random Forest Classifier
- XGBoost (final model)
- SHAP (SHapley Additive Explanations) for interpretability
- Hyperparameter tuning via GridSearchCV & RandomizedSearchCV

The goal was to balance **interpretability** with **predictive accuracy**, and produce a model that performs well while remaining explainable—critical in healthcare contexts.

---

## 📊 Dataset

- **Source:** UCI Machine Learning Repository  
- **Name:** Cleveland Heart Disease Dataset  
- **Samples:** 303  
- **Features:** 13 patient metrics (e.g., chest pain type, cholesterol, blood pressure, etc.)
- **Target:** Presence of heart disease (binary: 0 = no disease, 1 = disease)

---

## ⚙️ Methods & Tools

- `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`
- `xgboost` for gradient boosting classification
- `shap` for model interpretability
- Cross-validation with `GridSearchCV` and `RandomizedSearchCV`

---

## 📈 Key Results

- **Best Model:** XGBoost  
  - Accuracy: **0.87**  
  - F1-Score: **0.87** (macro & weighted average)

- **Top Features (by SHAP):**
  - `cp` (chest pain type)
  - `ca` (number of major vessels)
  - `thal` (thalassemia)
  - `thalach` (max heart rate)

- **Insights:**
  - SHAP confirmed that the model's most influential features aligned with medically relevant predictors.
  - Hyperparameter tuning significantly improved model consistency and performance.
  - Logistic Regression was interpretable but insufficient for complex patterns.

---

## 📚 Reflection

This project highlights the importance of not only building accurate models but also interpreting them in ways that **clinicians can trust**. Future directions include:
- Incorporating external datasets for validation
- Integrating domain-specific features (e.g., EHR data)
- Using tools like Optuna for automated hyperparameter optimization
- Deploying the model as a clinical decision support tool