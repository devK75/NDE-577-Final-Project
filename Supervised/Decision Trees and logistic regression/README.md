# Heart Failure Prediction Analysis

This project uses machine learning techniques to analyze and predict mortality caused by heart failure based on clinical records. The dataset contains demographic, medical, and laboratory information, allowing for insights into key factors associated with patient outcomes.

## Project Overview

The dataset includes 299 records with the following features:
- **Demographic Variables:**
  - Age, Sex
- **Medical Conditions:**
  - Anaemia, Diabetes, High Blood Pressure, Smoking
- **Laboratory Measurements:**
  - Creatinine Phosphokinase, Ejection Fraction, Platelets, Serum Creatinine, Serum Sodium
- **Other Information:**
  - Follow-up period (Time)
  - Death Event (target variable)

### Objective
The goal is to identify significant predictors of mortality and use machine learning models to predict heart failure outcomes accurately.

## Key Steps and Insights

### 1. Exploratory Data Analysis (EDA)
- **Descriptive Statistics:**
  - No missing values or null entries.
  - Dataset contains a mix of continuous and categorical variables.
- **Data Distributions:**
  - Age, creatinine phosphokinase, and serum creatinine are skewed distributions.
  - Ejection fraction and time show outliers, but they likely represent valid observations.
- **Correlation Analysis:**
  - No strong multicollinearity was observed among features.
- **Key Observations:**
  - Higher serum creatinine and lower follow-up time are associated with higher mortality rates.
  - Men have a higher survival rate compared to women.

### 2. Preprocessing
- **Scaling:**
  - Continuous features were standardized using `StandardScaler`.
- **Encoding:**
  - All categorical features were already numeric; no additional encoding was required.

### 3. Machine Learning Models
#### Logistic Regression
- Achieved **78% accuracy** with a **cross-validation score** of 74%.
- Showed higher precision and recall for predicting survival outcomes compared to death events.

#### Decision Tree Classifier
- Achieved **69% accuracy** with a **cross-validation score** of 64%.
- Less effective compared to logistic regression but useful for understanding variable importance.

### Model Comparison
- Logistic regression outperformed the decision tree in terms of accuracy, precision, and cross-validation.
- Both models demonstrate the ability to predict heart failure mortality, providing a foundation for further model optimization.

### Visualizations
- Heatmaps for feature correlation.
- Histograms for continuous variables (e.g., age, ejection fraction, serum sodium).
- Boxplots highlighting outliers in key variables.
- Scatter plots showing relationships between features and mortality (e.g., serum creatinine vs. death event).
- Pie charts summarizing categorical data distributions.

## Conclusion
This project highlights the potential of machine learning in predicting heart failure outcomes and identifying critical factors influencing patient mortality. Logistic regression provided the most accurate predictions, but further enhancements could yield even better results.


