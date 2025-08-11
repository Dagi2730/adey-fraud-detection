# Task 1: Data Analysis and Preprocessing

## Overview

This task involves comprehensive data analysis and preprocessing steps on the fraud detection dataset to prepare it for effective modeling. The goal is to clean the data, extract meaningful features, and transform the dataset to handle class imbalance and data inconsistencies.

---

## Steps Performed

### 1. Handling Missing Values
- Checked for missing values in the dataset.
- Dropped rows with missing data to maintain data integrity.

### 2. Data Cleaning
- Removed duplicate records to avoid bias.
- Corrected data types, especially converting date/time fields (`signup_time`, `purchase_time`) to datetime objects for accurate time-based analysis.

### 3. Exploratory Data Analysis (EDA)
- Performed univariate analysis on key features such as age, purchase value, and fraud class distribution.
- Conducted bivariate analysis to observe relationships, e.g., purchase value distribution by fraud class.

### 4. Geolocation Data Integration
- Converted IP addresses from the fraud dataset and IP range dataset into integer format for consistency.
- Merged datasets by mapping IP addresses to corresponding countries for geographic insights.

### 5. Feature Engineering
- Created time-based features including hour of day, day of week, and the duration between signup and purchase.
- Calculated transaction frequency and velocity per user using rolling windows over 24-hour periods to capture behavioral patterns.

### 6. Class Imbalance Analysis
- Analyzed the distribution of fraud vs non-fraud cases, confirming an imbalanced dataset.
- Visualized the imbalance for clearer understanding.

### 7. Data Transformation
- Encoded categorical variables using One-Hot Encoding to convert them into numerical format suitable for modeling.
- Normalized continuous numeric features with StandardScaler to ensure consistent feature scaling.

### 8. Handling Class Imbalance in Training
- Applied SMOTE (Synthetic Minority Oversampling Technique) on the training set only to address class imbalance without risking data leakage.
- Balanced the minority and majority classes to improve model learning.

---

## Justification of Techniques

- **Dropping missing values** was chosen over imputation to maintain data accuracy as missing values were minimal.
- **SMOTE** was applied to enhance the minority class representation, a common practice in fraud detection problems where fraud cases are rare.
- **StandardScaler** was used to normalize features for algorithms sensitive to scale differences.
- **One-Hot Encoding** allows machine learning models to interpret categorical variables effectively without introducing ordinal bias.

---

## Results Summary

- Cleaned dataset contains no missing values or duplicates.
- Integrated geographic data enriches fraud analysis by location.
- Engineered features capture temporal and behavioral transaction patterns.
- Balanced training data with SMOTE prepares the model for better fraud detection performance.

---

## Next Steps

Proceed to Task 2 for model training, evaluation, and optimization using the preprocessed and engineered dataset.
