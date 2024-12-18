# Heart Attack Prediction using Logistic Regression

This project aims to predict whether an individual is prone to a heart attack using classification models. The dataset contains patient records with demographic, clinical, and laboratory information, and the target variable indicates the likelihood of a heart attack.

## Project Overview

The dataset comprises 303 records with the following features:
- **Demographic Variables**:
  - `age`: Patient's age (continuous).
  - `sex`: Patient's sex (categorical).
- **Clinical Variables**:
  - `cp`: Chest pain type (categorical).
  - `trtbps`: Resting blood pressure (continuous).
  - `chol`: Cholesterol levels (continuous).
  - `fbs`: Fasting blood sugar > 120 mg/dL (categorical).
  - `restecg`: Resting electrocardiogram results (categorical).
  - `thalachh`: Maximum heart rate achieved (continuous).
  - `exng`: Exercise-induced angina (categorical).
  - `oldpeak`: Previous peak (continuous).
  - `slp`: Slope of peak exercise ST segment (categorical).
  - `caa`: Number of major vessels (continuous).
  - `thall`: Thalassemia (categorical).
- **Target Variable**:
  - `output`: Binary (1 = prone to heart attack, 0 = not prone).

### Objective
To analyze the dataset, preprocess the features, and train classification models to predict heart attack outcomes with high accuracy.

---

## Key Steps and Insights

### 1. Data Preprocessing
- **Categorical and Continuous Variables**:
  - Identified categorical and continuous variables.
  - Applied one-hot encoding for categorical variables.
- **Scaling**:
  - Standardized continuous variables using `StandardScaler` to ensure uniform feature scaling.

### 2. Exploratory Data Analysis (EDA)
- **Balanced Dataset**:
  - The target variable (`output`) was well-balanced, with a small difference between classes.
- **Distributions**:
  - Visualized distributions of continuous variables and relationships with the target variable.
- **Correlations**:
  - Correlation analysis revealed no significant multicollinearity among features.
  - The chest pain type (`cp`) had the strongest correlation with the target variable.
- **Key Observations**:
  - Individuals prone to heart attacks tended to have higher maximum heart rates (`thalachh`) and previous peak values (`oldpeak`).
  - Cholesterol levels (`chol`) increased with age for both classes.

### 3. Model Training and Evaluation
- **Models Used**:
  - Logistic Regression
  - Decision Tree Classifier
- **Results**:
  - Logistic Regression:
    - Accuracy: **82.4%**
    - Cross-validation score: **81.8%**
    - Outperformed Decision Tree Classifier in accuracy and F1-score.
  - Decision Tree Classifier:
    - Accuracy: **79.1%**
    - Cross-validation score: **74.8%**
    - Useful for feature importance analysis but less accurate than Logistic Regression.

- **Classification Metrics**:
  - Logistic Regression showed strong performance in precision, recall, and F1-score for both classes.
  - Confusion matrix analysis highlighted some misclassifications, especially for the minority class.

---

## Technologies Used
- **Python Libraries**:
  - `pandas` and `numpy` for data manipulation.
  - `matplotlib` and `seaborn` for visualizations.
  - `scikit-learn` for model training, scaling, and evaluation.
- **Models**:
  - Logistic Regression for baseline classification.
  - Decision Tree Classifier for comparison.

---

## Conclusion
This project highlights the utility of Logistic Regression for predicting heart attack risk with reasonable accuracy. While the analysis provided actionable insights into feature importance and classification metrics, future work could focus on enhancing the model's sensitivity to borderline cases and exploring more robust algorithms for healthcare applications.

