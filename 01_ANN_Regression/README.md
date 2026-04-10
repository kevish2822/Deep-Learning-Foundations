# ANN Regression – California Housing Price Prediction

## Overview

This project focuses on implementing an Artificial Neural Network (ANN) for a regression task using PyTorch.

The goal is to predict housing prices using the California Housing dataset while understanding how neural networks learn, generalize, and behave during training.

The project emphasizes building the model from scratch, analyzing training dynamics, and evaluating performance using appropriate metrics and visualizations.

---

## Dataset

The dataset used is the **California Housing Dataset**, which contains features such as:

- Median income
- House age
- Average rooms
- Population
- Location (latitude & longitude)

The target variable represents **median house value**.

---

## Data Preprocessing

The following preprocessing steps were performed:

- Train-test split
- Feature scaling using StandardScaler
- Conversion to PyTorch tensors
- Reshaping target variable for regression

Feature scaling was essential for stable and efficient neural network training.

---

## Model Architecture

The ANN model consists of:

- Input Layer: 8 features  
- Hidden Layer 1: 64 neurons (ReLU)  
- Hidden Layer 2: 32 neurons (ReLU)  
- Output Layer: 1 neuron (Regression output)

ReLU activation functions introduce non-linearity, allowing the network to learn complex patterns.

---

## Training Details

- Loss Function: Mean Squared Error (MSE)
- Optimizer: Adam
- Batch Size: 32
- Epochs: 100+

Training and validation losses were tracked across epochs to monitor learning behavior.

---

## Model Evaluation

The model was evaluated using:

- Mean Squared Error (MSE)
- R² Score
- Actual vs Predicted visualization
- Training vs Validation loss curves

---

## Results

- The model achieved a strong R² score, indicating good predictive performance.
- The loss curves show steady convergence during training.
- A gap between training and validation loss suggests slight overfitting.

---

## Observations

- Reducing batch size improved generalization performance.
- The model shows strong correlation between actual and predicted values.
- Predictions for higher target values show more variance due to dataset limitations.
- Slight overfitting is observed but remains within acceptable limits.

---

## Key Learning Outcomes

- Understanding how ANN works for regression tasks
- Importance of feature scaling in neural networks
- Effect of hyperparameters like batch size on performance
- Interpreting training vs validation loss behavior
- Evaluating regression models using MSE and R²
- Visualizing model performance effectively

---

## Dependencies

All required libraries are listed in the root `requirements.txt` file.