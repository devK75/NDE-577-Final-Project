# Neural Network Implementation: Recurrent Neural Networks (RNN)

This project implements a basic Recurrent Neural Network (RNN) to predict sequences and overcome challenges like the vanishing gradient problem. The project focuses on text data and includes a custom implementation of RNN layers, activation functions, and backpropagation through time (BPTT).

## Project Overview

Recurrent Neural Networks are powerful models for sequence prediction tasks, such as time-series forecasting and text generation. This project includes:
- A detailed explanation of the vanishing gradient problem and its solutions.
- A preprocessing pipeline for text data from Reddit comments.
- A custom RNN implementation, including forward propagation, backward propagation (BPTT), and training.

### Objectives
- Implement a custom RNN for sequence prediction.
- Train the model on tokenized text data to predict word sequences.
- Explore strategies to handle the vanishing gradient problem.

---

## Key Concepts and Features

### Vanishing Gradient Problem
- **Description**:
  - Occurs when gradients become too small during backpropagation, preventing effective weight updates.
  - Common in deep networks like RNNs.
- **Solutions**:
  - Use activation functions like ReLU/Leaky ReLU.
  - Employ LSTM/GRU architectures for their gradient-preserving mechanisms.
  - Gradient clipping to limit gradient magnitude.

### Data Preprocessing
- **Dataset**: Text data from a Reddit dataset (`reddit.csv`).
- **Steps**:
  - Tokenized sentences and added special tokens (`SENTENCE_START`, `SENTENCE_END`).
  - Built a vocabulary of 8,000 most frequent words.
  - Replaced rare words with an `UNKNOWN_TOKEN`.
  - Converted tokenized sentences into numerical sequences for training.

### RNN Implementation
- **Custom Classes**:
  - `RNNLayer`: Implements forward and backward passes for an RNN cell.
  - `MultiplyGate`, `AddGate`, `Tanh`, `Softmax`: Define the basic operations and activations.
- **Model Architecture**:
  - Input-to-Hidden (`U`), Hidden-to-Hidden (`W`), Hidden-to-Output (`V`) weight matrices.
  - Forward pass predicts word probabilities at each time step.
  - BPTT computes gradients for weights across time steps.
- **Training**:
  - Loss computed using cross-entropy.
  - Stochastic Gradient Descent (SGD) updates weights.
  - Adaptive learning rate adjusts based on loss trends.

---

## Results and Insights

### Training Results
- Trained the model on 100 sequences for 10 epochs with a learning rate of 0.005.
- Loss decreased consistently, demonstrating successful training:
  - Initial loss: **8.98**
  - Final loss: **5.66**

### Key Observations
- Custom RNN implementation effectively learned sequence patterns from text.
- Challenges like the vanishing gradient were managed using small sequence lengths and gradient clipping.

---

## Technologies Used

- **Python Libraries**:
  - `numpy` for numerical operations.
  - `nltk` for text tokenization and preprocessing.
  - `matplotlib` for loss visualization.


