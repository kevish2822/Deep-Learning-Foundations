# CNN Image Classification – CIFAR-10

## Overview

This project focuses on implementing a Convolutional Neural Network (CNN) for multi-class image classification using PyTorch.

The goal is to classify images from the CIFAR-10 dataset into 10 different categories while understanding how convolutional layers extract features and how deep learning models generalize.

---

## Dataset

The dataset used is the **CIFAR-10 dataset**, which consists of:

- 60,000 color images (32×32)
- 10 classes:
  - Airplane, Automobile, Bird, Cat, Deer
  - Dog, Frog, Horse, Ship, Truck

---

## Data Preprocessing

The following preprocessing techniques were applied:

- Data augmentation:
  - Random Horizontal Flip
  - Random Cropping with padding
- Conversion to tensors
- Normalization of pixel values
- Batch loading using DataLoader

Data augmentation was used to improve generalization and reduce overfitting.

---

## Model Architecture

The CNN model consists of:

- Convolutional layers:
  - Conv(3 → 32) → ReLU → MaxPool
  - Conv(32 → 64) → ReLU → MaxPool
  - Conv(64 → 128) → ReLU → MaxPool

- Fully connected layers:
  - Flatten
  - Linear → ReLU
  - Output layer (10 classes)

The model extracts spatial features using convolution and performs classification using fully connected layers.

---

## Training Details

- Loss Function: CrossEntropyLoss
- Optimizer: Adam
- Batch Size: 64
- Epochs: ~10
- Model checkpointing based on lowest validation loss

Training and validation losses were tracked to monitor model performance.

---

## Model Evaluation

The model was evaluated using:

- Accuracy
- Confusion Matrix
- Sample Predictions (visualization)

---

## Results

- The model achieves good classification accuracy on CIFAR-10
- Data augmentation significantly reduced overfitting
- Validation loss trends indicate improved generalization compared to baseline

---

## Observations

- Early epochs capture general patterns effectively
- Data augmentation improves model robustness
- Some classes are harder to distinguish due to visual similarity (e.g., cat vs dog)
- Overfitting is reduced but still present to a small extent

---

## Key Learning Outcomes

- Understanding convolutional neural networks
- Importance of feature extraction in images
- Role of data augmentation in improving performance
- Difference between binary and multi-class classification
- Interpreting confusion matrices and predictions
- Handling overfitting in deep learning models

---

## Dependencies

All required libraries are listed in the `requirements.txt` file.