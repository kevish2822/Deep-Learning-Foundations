# ANN Classification – Breast Cancer Prediction

## Overview

This project focuses on implementing an Artificial Neural Network (ANN) for a binary classification task using PyTorch.

The objective is to classify tumors as malignant or benign using the Breast Cancer Wisconsin dataset while understanding neural network behavior, training dynamics, and evaluation techniques.

The project emphasizes correct loss function usage, model evaluation, and handling overfitting.

---

## Dataset

The dataset used is the **Breast Cancer Wisconsin Dataset**, which contains 30 numerical features computed from digitized images of breast masses.

The target variable is binary:
- 0 → Malignant
- 1 → Benign

---

## Data Preprocessing

The following preprocessing steps were performed:

- Train-test split
- Feature scaling using StandardScaler
- Conversion to PyTorch tensors
- Reshaping target variable for compatibility with loss function
- Use of DataLoader for batch training

Feature scaling is critical for stable neural network training.

---

## Model Architecture

The ANN model consists of:

- Input Layer: 30 features  
- Hidden Layer 1: 64 neurons (ReLU)  
- Hidden Layer 2: 32 neurons (ReLU)  
- Hidden Layer 3: 16 neurons (ReLU)  
- Hidden Layer 4: 8 neurons (ReLU)  
- Output Layer: 1 neuron (Binary output)

No activation function is used in the output layer as **BCEWithLogitsLoss** is applied.

---

## Training Details

- Loss Function: Binary Cross Entropy with Logits (BCEWithLogitsLoss)
- Optimizer: Adam
- Batch Size: 32
- Epochs: 100
- Model checkpointing based on best validation accuracy

Training and validation performance were tracked across epochs.

---

## Model Evaluation

The model was evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix
- Training vs Validation Loss curves

---

## Results

- The model achieved very high accuracy (~99%)
- Early convergence observed (best performance around early epochs)
- Training loss decreases continuously
- Validation loss increases after initial epochs, indicating slight overfitting

---

## Observations

- The dataset is well-structured and easily separable, leading to high performance
- The model begins to overfit after a certain number of epochs
- Proper use of BCEWithLogitsLoss improves numerical stability
- Thresholding sigmoid outputs is necessary for classification metrics

---

## Key Learning Outcomes

- Understanding ANN for classification tasks
- Correct use of BCEWithLogitsLoss and logits
- Importance of output transformations (sigmoid + thresholding)
- Detecting and interpreting overfitting using loss curves
- Evaluating classification models using multiple metrics
- Importance of balancing model complexity with dataset characteristics

---

## Dependencies

All required libraries are listed in the root `requirements.txt` file.