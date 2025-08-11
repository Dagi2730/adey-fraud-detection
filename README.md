# Task 2 - Model Building and Training

## Overview

This task involves building and evaluating predictive models for fraud detection using a labeled dataset. The objective is to accurately identify fraudulent transactions despite class imbalance in the data.

---

## Data Preparation

- Separate features (`X`) and target (`y`) variables.
- Perform stratified train-test split to maintain fraud ratio.
- Preprocessing steps:
  - Impute missing numerical values using median strategy.
  - Scale numerical features with `StandardScaler`.
  - One-hot encode categorical features.
- Fit preprocessors on training data only, then transform test data to avoid data leakage.

---

## Models Built

Two models were developed and compared:

1. **Logistic Regression**  
   A simple, interpretable baseline model.

2. **Random Forest Classifier**  
   A powerful ensemble model suitable for imbalanced datasets.

---

## Evaluation Metrics

Models are evaluated using metrics suitable for imbalanced classification:

- **Average Precision Score (AUC-PR)** – summarizes precision-recall tradeoff.
- **F1 Score** – harmonic mean of precision and recall.
- **Confusion Matrix** – detailed breakdown of true/false positives and negatives.

Precision-Recall curves are also generated for visual analysis.

---

## Results and Conclusion

- Models are trained on training data and evaluated on the test set.
- Performance comparison is based on AUC-PR and F1 scores.
- The best performing model is recommended for deployment considering both precision and recall.

---

## Usage

1. Load and split data.
2. Apply preprocessing.
3. Train and evaluate models with provided scripts or notebooks.

---

## Dependencies

- Python 3.7 or higher
- pandas
- numpy
- scikit-learn
- matplotlib

---

For any questions or feedback, please feel free to contact.

