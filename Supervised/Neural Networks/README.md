# Employee Retention Prediction using Logistic Regression

This project analyzes HR data to predict employee turnover based on factors such as job satisfaction, performance, and salary. A Logistic Regression model is employed to classify whether an employee will leave the company (`left = 1`) or stay (`left = 0`).

## Project Overview

The dataset consists of 14,999 employee records with the following features:
- **Quantitative Variables**:
  - `satisfaction_level`: Job satisfaction level.
  - `last_evaluation`: Last performance evaluation score.
  - `number_project`: Number of projects assigned.
  - `average_monthly_hours`: Average hours worked per month.
  - `time_spend_company`: Number of years spent in the company.
- **Qualitative Variables**:
  - `Work_accident`: Whether the employee experienced a workplace accident (binary).
  - `left`: Target variable indicating if the employee left (binary).
  - `promotion_last_5years`: Whether the employee was promoted in the last five years (binary).
  - `sales`: Department of the employee.
  - `salary`: Salary level (categorical: low, medium, high).

### Objective
To identify key factors influencing employee turnover and build a predictive model to classify employee retention.

---

## Key Steps and Insights

### 1. Data Preprocessing
- **Missing Values**:
  - No missing values were found in the dataset.
- **Feature Engineering**:
  - Created dummy variables for categorical features (`sales`, `salary`) using one-hot encoding.
  - Standardized quantitative features using `StandardScaler` for uniform scaling.

### 2. Exploratory Data Analysis (EDA)
- **Retention vs. Turnover**:
  - Majority of employees (76%) stayed with the company.
  - 24% of employees left.
- **Key Observations**:
  - Employees who left had:
    - Lower job satisfaction levels.
    - Higher last evaluation scores and more projects.
    - Higher average monthly hours.
  - Employees in sales and technical roles, with low salaries, were more likely to leave.
  - No employees who left had received a promotion in the last five years.

- **Visualizations**:
  - Box plots for quantitative variables (e.g., satisfaction level, time spent).
  - Count plots for categorical variables (e.g., salary, department).
  - Correlation heatmap showed moderate relationships between some features.

### 3. Model Training and Evaluation
- **Model**: Logistic Regression.
- **Data Split**:
  - Training: 70%
  - Testing: 30%
- **Accuracy**:
  - Logistic Regression achieved an accuracy of **78.6%** on the test set.
- **Feature Importance**:
  - StandardScaler improved model performance by normalizing feature ranges.
  - Dummy variables for categorical features captured important patterns, especially for `salary` and `sales`.

---

## Technologies Used
- **Python Libraries**:
  - `pandas` and `numpy` for data manipulation.
  - `seaborn` and `matplotlib` for visualizations.
  - `scikit-learn` for model building and evaluation.
- **Model**:
  - Logistic Regression for binary classification.

## Conclusion
This project highlights the potential of Logistic Regression in predicting employee turnover and understanding retention factors. While the model achieves reasonable accuracy, future improvements could focus on advanced algorithms and addressing data imbalances for more robust predictions.
