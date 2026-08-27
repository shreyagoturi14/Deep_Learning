# Customer Churn Prediction using ANN

## Overview

This project implements an **Artificial Neural Network (ANN)** to predict customer churn using customer banking information.

Customer churn prediction is a common real-world business problem where organizations identify customers who are likely to leave their service. Early identification of potential churners can help businesses take appropriate retention actions.

In this project, an ANN is trained on customer information to perform **binary classification**:

* `0` → Customer stayed
* `1` → Customer exited
* 
## 🎯 Objective

The objective of this project is to build a neural network that learns patterns from customer attributes and predicts whether a customer is likely to leave the bank.

### Input Features
The model uses the following 8 features:

* Credit Score
* Age
* Tenure
* Balance
* Number of Products
* Has Credit Card
* Is Active Member
* Estimated Salary

### Target

**Exited**

* `0` → Customer stayed
* `1` → Customer exited

---

## 🧠 Artificial Neural Network

An **Artificial Neural Network (ANN)** is a machine learning model inspired by the structure of biological neural networks.

An ANN consists of interconnected neurons organized into layers. Each neuron receives inputs, applies weights and bias, and passes the result through an activation function.

### Basic Flow

**Input Features → Hidden Layers → Output Layer → Prediction**

In this project, the ANN learns the relationship between customer attributes and churn behavior.

---

## 🏗️ Model Architecture

The implemented ANN contains:

| Layer          |    Neurons | Activation |
| -------------- | ---------: | ---------- |
| Input          | 8 features | —          |
| Hidden Layer 1 |          6 | ReLU       |
| Hidden Layer 2 |          4 | ReLU       |
| Hidden Layer 3 |          2 | ReLU       |
| Output Layer   |          1 | Sigmoid    |

### Architecture

```text
8 Input Features
       ↓
Dense Layer (6 neurons, ReLU)
       ↓
Dense Layer (4 neurons, ReLU)
       ↓
Dense Layer (2 neurons, ReLU)
       ↓
Output Layer (1 neuron, Sigmoid)
       ↓
Churn Prediction (0 / 1)
```

---

## ⚙️ Implementation Steps

### 1. Data Loading

The banking customer churn dataset is loaded using Pandas.

### 2. Data Preparation

Unnecessary columns such as `RowNumber`, `CustomerId`, and `Surname` are removed.

The dataset is then divided into input features and the target variable.

### 3. Feature Scaling

`StandardScaler` is used to standardize the input features so that features with different numerical ranges can be processed effectively by the neural network.

### 4. Train-Test Split

The dataset is divided into:

* **80% Training Data → 8,000 records**
* **20% Testing Data → 2,000 records**

### 5. ANN Construction

The neural network is created using **Keras/TensorFlow** with multiple dense layers and ReLU activation functions.

### 6. Model Compilation

The model uses:

* **Optimizer:** Adam
* **Loss Function:** Binary Cross-Entropy
* **Metric:** Accuracy

### 7. Model Training

The ANN is trained using:

* **Epochs:** 50
* **Batch Size:** 100

### 8. Prediction

The trained model generates a probability for each customer.

A threshold of `0.5` is used to convert the probability into a binary prediction:

```text
Probability > 0.5 → 1 (Exited)
Probability ≤ 0.5 → 0 (Stayed)
```

---

## 📊 Results

The model achieved the following accuracy:

| Dataset  |   Accuracy |
| -------- | ---------: |
| Training | **85.19%** |
| Testing  | **85.75%** |

The testing accuracy is slightly higher than the training accuracy in this run. This can occur due to the particular train-test split and model behavior; it does not by itself indicate a problem.

---

## 🌍 Real-World Application

Customer churn prediction can help organizations identify customers who may be at risk of leaving.

For example:

```text
Customer Data
     ↓
ANN Model
     ↓
Churn Probability
     ↓
High Risk / Low Risk
     ↓
Customer Retention Strategy
```

A bank could use such a system to identify potentially dissatisfied customers and offer appropriate retention measures such as personalized services, improved support, or suitable product recommendations.

The same concept can be applied in:

* Banking
* Telecom
* Insurance
* Subscription services
* E-commerce
* SaaS businesses

---

## ✅ Advantages of ANN for Churn Prediction

* Can learn complex relationships between multiple customer features
* Handles multiple input variables simultaneously
* Useful for non-linear classification problems
* Can be extended with additional features and deeper architectures
* Provides a foundation for understanding modern deep learning models

## ⚠️ Limitations

* Requires appropriate preprocessing and feature scaling
* Model performance depends on the quality and representativeness of the data
* Neural networks can overfit if not properly regularized
* Accuracy alone may not be sufficient for evaluating churn prediction
* ANN predictions can be less interpretable than simpler models

---

## 🛠️ Technologies Used

* **Python**
* **Pandas** — Data loading and manipulation
* **NumPy** — Numerical operations
* **Scikit-learn** — Data preprocessing, train-test split, and evaluation
* **TensorFlow / Keras** — ANN implementation and training

---

## 📁 Project Structure

```text
Customer-Churn-Prediction-ANN/
│
├── Customer Churn Prediction using ANN.ipynb
└── README.md
```

---

## 🎓 Key Learnings

Through this project, I gained practical experience in:

* Building an Artificial Neural Network
* Preparing data for deep learning
* Feature scaling using StandardScaler
* Splitting data into training and testing sets
* Designing dense neural-network layers
* Understanding ReLU and Sigmoid activation functions
* Using Adam optimization
* Using Binary Cross-Entropy loss
* Training an ANN using epochs and batches
* Converting prediction probabilities into binary classes
* Evaluating a classification model

---

## 🚀 Future Improvements

Possible improvements to this project include:

* Confusion Matrix
* Precision, Recall and F1-Score
* ROC-AUC evaluation
* Hyperparameter tuning
* Dropout and regularization
* Experimenting with different ANN architectures
* Comparing ANN performance with traditional machine learning models

---

## 📌 Conclusion

This project demonstrates how an **Artificial Neural Network can be applied to a real-world classification problem** such as customer churn prediction.

It provides a practical foundation for understanding how neural networks process structured data, learn patterns through multiple layers, and generate predictions for business decision-making.

