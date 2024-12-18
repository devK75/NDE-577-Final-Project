# NDE-577-Final-Project
# NDE-577 Final Project

This repository contains the implementation and analysis of various machine learning algorithms, exploring both supervised and unsupervised learning techniques. The project spans multiple models and methodologies, highlighting their applications, strengths, and limitations.

---

## Table of Contents

1. [Project Overview](#project-overview)
2. [Algorithms Covered](#algorithms-covered)
    - [Supervised Learning](#supervised-learning)
    - [Unsupervised Learning](#unsupervised-learning)
3. [Datasets Used](#datasets-used)
4. [Technologies](#technologies)

---

## Project Overview

The project demonstrates the implementation of foundational and advanced machine learning algorithms, emphasizing their theoretical underpinnings, practical applications, and performance evaluation. It is divided into supervised and unsupervised learning categories.

Key focus areas include:
- Data preprocessing and feature engineering.
- Model training, testing, and evaluation.
- Comparative analysis of algorithms.
- Insights into the limitations and improvements for real-world applications.

---

## Algorithms Covered

### Supervised Learning

1. **Linear Regression**:
   - Predicted numerical outcomes (e.g., bike rentals).
   - Explored feature relationships and model coefficients.
   - Achieved an R² score of 33%.

2. **Logistic Regression**:
   - Used for binary classification (e.g., heart disease prediction, employee attrition).
   - Achieved up to 82% accuracy with detailed insights into feature importance.

3. **Perceptron**:
   - Built a binary classifier for linearly separable data.
   - Achieved 100% accuracy on a simple dataset with a visualized decision boundary.

4. **Decision Trees and Random Forests**:
   - Applied to car evaluation classification.
   - Decision Tree: 76.88% accuracy with interpretable results.
   - Random Forest: 97.88% accuracy, emphasizing robustness and generalization.

### Unsupervised Learning

1. **K-Means Clustering**:
   - Segmented wholesale customer data.
   - Identified optimal clusters using the elbow method.

2. **DBSCAN Clustering**:
   - Explored density-based clustering for customer segmentation.
   - Highlighted sensitivity to parameter tuning.

3. **Dimensionality Reduction (PCA)**:
   - Reduced features for better visualization and clustering.

4. **Neural Networks**:
   - Implemented a custom RNN for sequence prediction (e.g., text data).
   - Addressed the vanishing gradient problem with insights into LSTM advantages.

---

## Datasets Used

1. **Bike Rentals**: Numerical dataset for predicting rental counts based on weather and temporal features.
2. **Heart Disease Dataset**: Medical data for binary classification tasks.
3. **HR Analytics**: Employee records for attrition analysis.
4. **Car Evaluation**: Categorical dataset for classifying car conditions.
5. **Wholesale Customers**: Dataset for clustering and segmentation.
6. **Reddit Comments**: Sequence data for RNN text prediction.

---

## Technologies

- **Programming Language**: Python
- **Libraries**:
  - `numpy`, `pandas` for data manipulation.
  - `matplotlib`, `seaborn` for visualization.
  - `scikit-learn` for model implementation.
  - `nltk` for text processing (RNN project).

