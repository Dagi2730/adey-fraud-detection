# Task 3: Model Explainability with SHAP

## Overview

This task focuses on interpreting the best-performing fraud detection model using SHAP (Shapley Additive exPlanations). SHAP provides a unified measure of feature importance that explains individual predictions by quantifying the contribution of each feature.

## Objectives

- Use SHAP to explain the Random Forest classifier trained for fraud detection.
- Generate global explanations to identify the most important features influencing predictions.
- Produce local explanations (force plots) to understand individual prediction details.
- Interpret SHAP visualizations to gain actionable insights about key fraud drivers.

## Implementation Details

- **Model**: Random Forest classifier trained on preprocessed transaction data.
- **SHAP Explainer**: `TreeExplainer` initialized with a representative background dataset.
- **Global Explanation**: SHAP summary plots highlighting top features by average absolute SHAP values.
- **Local Explanation**: SHAP force plots for detailed per-instance interpretation.
- **Preprocessing**: Imputation, scaling, and one-hot encoding consistent with model training.

## How to Run

1. Load the trained Random Forest model and preprocessing objects.
2. Compute SHAP values on a sample of the test data.
3. Generate SHAP summary plots for global feature importance.
4. Generate and save SHAP force plots for local explanations.
5. Analyze printed feature importance and visualizations to understand fraud drivers.

## Insights

- SHAP summary plots reveal which features have the greatest influence on fraud predictions.
- Force plots provide explanations for individual transaction predictions, showing the impact of each feature.
- These insights improve model transparency and can guide further fraud detection strategies.

## Files

- `rf_task2.pkl` — Trained Random Forest model file.
- `preproc_task2.joblib` — Saved preprocessing pipeline objects.
- `shap_force_plot_instance.html` — Interactive force plot for a single prediction.
- `notebooks/task3_shap_explainability.ipynb` — Notebook implementing SHAP-based explanations.

---


