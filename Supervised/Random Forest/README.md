# Car Evaluation with Decision Tree and Random Forest Classifiers

This project demonstrates the application of Decision Tree and Random Forest classifiers to analyze and classify car evaluations based on multiple categorical features. The dataset provides a structured classification problem, enabling the comparison of these two machine learning algorithms in terms of accuracy, interpretability, and robustness.

---

## Project Overview

The dataset consists of 1,728 records with the following features:
- **Features**:
  - `buying`: Buying price of the car (categorical).
  - `maint`: Maintenance cost (categorical).
  - `doors`: Number of doors (categorical).
  - `persons`: Number of persons the car can carry (categorical).
  - `lug_boot`: Size of luggage boot (categorical).
  - `safety`: Safety level (categorical).
- **Target**:
  - `class`: Car evaluation outcome (`unacc`, `acc`, `good`, `vgood`).

### Objectives
1. Preprocess and encode categorical data for machine learning.
2. Train and evaluate a Decision Tree classifier and Random Forest classifier.
3. Compare the performance and interpretability of the models.

---

## Key Steps and Insights

### 1. Data Preprocessing
- **Encoding**: Converted categorical features into numerical values using mappings:
  - Example: `buying = {'low': 0, 'med': 1, 'high': 2, 'vhigh': 3}`.
- **Feature and Target Splits**:
  - `X`: Features (`buying`, `maint`, `doors`, `persons`, `lug_boot`, `safety`).
  - `y`: Target (`class`).

### 2. Models and Performance

#### Decision Tree Classifier
- **Configuration**:
  - Criterion: Gini Index
  - Maximum Depth: 3
- **Performance**:
  - Test Accuracy: **76.88%**
- **Insights**:
  - Highlighted feature importance: `safety` and `persons` were critical for classification.
  - Limited depth resulted in some underfitting, as shown by discrepancies between training and testing performance.
- **Visualization**:
  - Tree structure visualized to interpret decision splits.

#### Random Forest Classifier
- **Configuration**:
  - Number of Estimators: 100
  - Random State: 0
- **Performance**:
  - Test Accuracy: **97.88%**
- **Insights**:
  - Demonstrated superior performance by combining predictions from multiple decision trees.
  - Robustness and generalization capabilities effectively reduced overfitting.

---

## Key Insights and Comparisons

| **Model**            | **Criterion** | **Max Depth/Estimators** | **Accuracy**  | **Strengths**             | **Limitations**              |
|-----------------------|---------------|--------------------------|---------------|---------------------------|------------------------------|
| **Decision Tree**     | Gini Index    | Depth = 3               | 76.88%        | Interpretable and simple  | Struggles with complex data |
| **Random Forest**     | Ensemble      | 100 Estimators          | 97.88%        | High accuracy, robust     | Less interpretable          |

- **Feature Importance**:
  - Both models emphasized `safety` and `persons` as critical features.
  - Random Forest provided a more comprehensive feature importance analysis due to its ensemble nature.

---

## Technologies Used
- **Python Libraries**:
  - `pandas` and `numpy` for data manipulation.
  - `matplotlib` and `seaborn` for visualizations.
  - `scikit-learn` for model training and evaluation.
- **Algorithms**:
  - Decision Tree
  - Random Forest

