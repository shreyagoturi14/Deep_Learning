# Single Layer Perceptron

## Overview
A Single-Layer Perceptron (SLP) is one of the simplest forms of a neural network, mainly used for binary classification.

It consists of the following components:

Inputs (x₁, x₂, ...)
The input features provided to the model. In this project, the inputs are CGPA and IQ.
Weights (w₁, w₂, ...) and Bias (b)
Parameters learned during training. They determine the importance of each input and help the model learn a suitable decision boundary.

Net Input Calculation
The perceptron calculates the weighted sum of the inputs and adds the bias:

Net Input = (w₁ × x₁) + (w₂ × x₂) + b

Activation Function
A step (threshold) function converts the net input into a binary prediction:
1 → Placed
0 → Not Placed

## Concept
A perceptron is a simple neural-network model that calculates a weighted sum of input features along with a bias and applies an activation function to produce a prediction.

**Basic flow:**

`Input Features → Weighted Sum + Bias → Activation Function → Prediction`

The model learns the weights during training by adjusting them when it makes incorrect predictions.

## What I Implemented
The notebook covers the following steps:

1. Loaded the placement dataset using Pandas.
2. Removed the unnecessary index column.
3. Selected **CGPA** and **IQ** as input features.
4. Used **Placement** as the target variable.
5. Visualized the relationship between the features and target.
6. Split the dataset into training and testing sets.
7. Implemented the Perceptron using **Scikit-learn**.

## Real-World Applications

A perceptron can be used for simple binary classification problems such as:

* Spam vs. non-spam classification
* Pass vs. fail prediction
* Defective vs. non-defective products
* Simple approval/rejection systems
* Basic risk classification

However, modern real-world applications with complex data generally require more advanced machine learning or deep learning models.

## Advantages

* Simple and easy to understand
* Fast to train
* Computationally lightweight
* Suitable for simple binary classification
* Helps build the foundation for understanding neural networks

## Limitations

* Can learn only **linearly separable patterns**
* Cannot solve non-linear problems such as XOR
* Not suitable for complex data such as images, audio, or natural language
* Limited compared with modern multi-layer neural networks

## Technologies Used

* Python
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn

## Key Learning

This project helped me understand the basic working of a neural-network model, including **features, weights, bias, activation, training, and binary classification**, and provides a foundation for learning more advanced neural networks and deep learning architectures.
