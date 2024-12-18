# Diabetes Prediction using K-Nearest Neighbors (KNN)

This project applies the K-Nearest Neighbors (KNN) algorithm to classify individuals as diabetic or non-diabetic using a dataset containing various health-related metrics. The analysis focuses on data preprocessing, exploratory data analysis, and optimizing the KNN model for improved classification accuracy.

## Project Overview

The dataset contains 768 records with the following features:
- **Pregnancies**: Number of pregnancies.
- **Glucose**: Plasma glucose concentration after a glucose tolerance test.
- **BloodPressure**: Diastolic blood pressure (mm Hg).
- **SkinThickness**: Triceps skinfold thickness (mm).
- **Insulin**: 2-hour serum insulin (mu U/ml).
- **BMI**: Body Mass Index.
- **DiabetesPedigreeFunction**: Diabetes pedigree function score.
- **Age**: Patient's age.
- **Outcome**: Binary classification (1 = diabetic, 0 = non-diabetic).

### Objectives
- Clean and preprocess the data to handle missing or invalid values.
- Explore the relationships between features using visualizations and statistics.
- Train and optimize a KNN model for accurate diabetes prediction.
- Evaluate the model's performance and identify areas for improvement.

## Key Steps and Insights

### 1. Data Preprocessing
- Replaced zero values in `Glucose`, `BloodPressure`, `SkinThickness`, `Insulin`, and `BMI` with `NaN`.
- Imputed missing values using:
  - Mean for `Glucose` and `BloodPressure`.
  - Median for `SkinThickness`, `Insulin`, and `BMI`.
- Scaled all features using `StandardScaler` for uniformity in the distance-based KNN algorithm.

### 2. Exploratory Data Analysis (EDA)
- **Histograms** revealed the distributions of key features.
- **Scatter plots** highlighted relationships among variables (e.g., `SkinThickness` vs. `Insulin`).
- **Correlation Matrix** showed moderate correlations among certain features, such as `BMI` and `Glucose`.
- **Class Distribution**: The dataset exhibited class imbalance, with fewer diabetic cases (`Outcome = 1`).

### 3. KNN Model Optimization
- Tested K values ranging from 1 to 20:
  - Training accuracy decreased with larger K values, reducing overfitting.
  - Testing accuracy peaked at **K = 11**, achieving a test accuracy of **75.3%**.
- Final KNN model performed as follows:
  - **Non-diabetic class (Outcome = 0):** High precision and recall.
  - **Diabetic class (Outcome = 1):** Lower precision and recall, indicating challenges in detecting diabetic cases.

### 4. Model Evaluation
- **Confusion Matrix**:
  - Correctly predicted 127 non-diabetic cases and 47 diabetic cases.
  - Misclassified 34 diabetic cases as non-diabetic.
- **Classification Report**:
  - Overall accuracy: **75%**.
  - Weighted F1-score: **0.75**.
  - Recall for diabetic cases: **58%**, highlighting sensitivity issues.

### 5. Observations and Recommendations
- Class imbalance likely impacted model sensitivity for diabetic predictions.
- Improvements could include:
  - Oversampling the minority class or undersampling the majority class.
  - Feature engineering to explore interactions (e.g., `Glucose` and `BMI`).
  - Trying alternative algorithms like Random Forest or Gradient Boosting.

## Visualizations
- **Histograms**: Feature distributions (e.g., `Glucose`, `BMI`).
- **Scatter Plots**: Relationships between key variables.
- **Heatmaps**: Correlation matrix of features.
- **Line Plot**: K values vs. training and testing accuracy.

## Technologies Used
- **Python Libraries**:
  - `pandas` and `numpy` for data manipulation.
  - `matplotlib` and `seaborn` for visualization.
  - `scikit-learn` for model building, evaluation, and preprocessing.
- **Algorithm**:
  - K-Nearest Neighbors (KNN)



## Conclusion
The KNN algorithm provides a solid baseline for diabetes prediction with high accuracy for non-diabetic cases. However, improvements are needed to enhance sensitivity for diabetic cases. This project demonstrates the importance of careful preprocessing, model optimization, and evaluation in healthcare-related machine learning applications.


