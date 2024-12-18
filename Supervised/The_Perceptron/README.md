# Perceptron Algorithm for Binary Classification

This project implements the Perceptron algorithm, a foundational linear classifier, to classify data into two classes. The dataset consists of features and labels suitable for binary classification tasks, demonstrating the model's ability to learn a linear decision boundary.

---

## Project Overview

The Perceptron is a simple yet powerful supervised learning algorithm for binary classification. This project involves:
1. Splitting the dataset into training and testing sets.
2. Normalizing the features for numerical stability.
3. Implementing and training a Perceptron model.
4. Evaluating the model and visualizing its decision boundary.

### Objectives
- Build a Perceptron model from scratch.
- Train the model to classify linearly separable data.
- Evaluate the model’s performance and visualize its decision boundary.

---

## Key Steps and Insights

### 1. Dataset Preparation
- **Source**: Data loaded from `data.txt` (tab-delimited).
- **Features and Labels**:
  - `X`: Feature matrix of shape (100, 2).
  - `Y`: Labels vector of shape (100,).
- **Train-Test Split**:
  - 80% of the data used for training.
  - 20% used for testing.

### 2. Data Normalization
- Features were normalized using z-score normalization:
  - \( X_{\text{normalized}} = \frac{X - \mu}{\sigma} \)
- Ensured mean = 0 and standard deviation = 1 for stable convergence.

### 3. Perceptron Implementation
- **Initialization**:
  - Weights and bias initialized to small random values.
- **Forward Pass**:
  - Computed a linear combination of weights and inputs:
    \( \text{linear} = X \cdot W + b \)
  - Applied a step function to generate binary predictions.
- **Backward Pass**:
  - Errors computed as the difference between true labels and predictions.
  - Updated weights and bias:
    \( W = W + \eta \cdot \text{error} \cdot X \)
    \( b = b + \eta \cdot \text{error} \)
- **Training**:
  - Model trained for 5 epochs with a learning rate (\(\eta\)) of 0.001.

### 4. Results
- **Training and Testing Accuracy**:
  - Achieved 100% accuracy on both training and testing sets.
- **Decision Boundary**:
  - Visualized a linear boundary separating the two classes, demonstrating the model's ability to classify linearly separable data effectively.

### 5. Key Observations
- The Perceptron performed exceptionally well for this dataset due to its linear separability.
- The decision boundary clearly divided the two classes, as shown in the visualizations.
- Limitations:
  - The Perceptron is suitable only for linearly separable data. Nonlinear datasets require advanced models like SVMs or neural networks.

---

## Technologies Used

- **Python Libraries**:
  - `numpy` for numerical computations.
  - `matplotlib` for data and decision boundary visualizations.
- **Machine Learning**:
  - Custom implementation of the Perceptron algorithm.

