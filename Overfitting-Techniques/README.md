# Overfitting Techniques in Deep Learning

## Overview

This project demonstrates **Overfitting in Artificial Neural Networks (ANNs)** and explores different techniques used to reduce overfitting and improve model generalization.

The following techniques are implemented using TensorFlow/Keras:

- Early Stopping
- L2 Regularization
- Batch Normalization

---

## What is Overfitting?

**Overfitting** occurs when a model learns the training data too closely and performs poorly on unseen data.

The goal is to build a model that learns useful patterns and **generalizes well to new data**.

---

## Techniques Covered

### 1. Early Stopping

Stops model training when validation performance stops improving.

**Purpose:** Prevent unnecessary training and reduce overfitting.

### 2. L2 Regularization

Adds a penalty for large model weights to control the complexity of the neural network.

**Purpose:** Encourage simpler models and improve generalization.

### 3. Batch Normalization

Normalizes intermediate activations within mini-batches during training.

**Purpose:** Improve training stability and efficiency, with potential regularizing effects.

---

## Project Structure

```text
Overfitting-Techniques/
│
├── Overfitting_Early_Stopping.ipynb
├── Overfitting_Regularization.ipynb
├── Overfitting_Batch_Normalization.ipynb
│
└── README.md
