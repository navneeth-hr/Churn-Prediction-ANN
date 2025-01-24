# Customer Churn Prediction using Artificial Neural Network (ANN)

This project implements an **Artificial Neural Network (ANN)** to predict customer churn for a bank. The goal is to determine whether a customer will leave the bank based on various features such as credit score, geography, gender, age, balance, etc.

## Table of Contents
1. [Project Overview](#project-overview)
2. [Code Explanation](#code-explanation)
3. [Results](#results)
4. [How to Run the Code](#how-to-run-the-code)
5. [Dependencies](#dependencies)

## Project Overview
- **Objective**: Predict whether a customer will leave the bank (churn) based on their demographic and financial data.
- **Dataset**: `Churn_Modelling.csv` (contains customer information such as credit score, geography, gender, age, balance, etc.).
- **Model**: Artificial Neural Network (ANN) built using TensorFlow/Keras.
- **Evaluation**: Accuracy and Confusion Matrix.


## Code Explanation
1. **Data Preprocessing**:
   - Load and preprocess the dataset.
   - Encode categorical variables (Gender, Geography).
   - Split the dataset into training and testing sets.
   - Scale the features using `StandardScaler`.

2. **Exploratory Data Analysis (EDA)**:
   - Visualize correlations between features using a heatmap.
   - Create pairplots to understand relationships between features.

3. **Feature Selection**:
   - Use Random Forest to rank feature importance.
   - Select the top 10 features for training the ANN.

4. **Building the ANN**:
   - Define the ANN architecture (2 hidden layers, 1 output layer).
   - Perform hyperparameter tuning to find the best model.

5. **Evaluating the Model**:
   - Evaluate the model using a confusion matrix and accuracy score.

6. **Making Predictions**:
   - Predict whether a single customer will leave the bank.


## Results

- **Best Hyperparameters**:
  - Optimizer: `adam`
  - Units: `6`
  - Batch Size: `64`
  - Epochs: `100`
- **Best Accuracy**: **86.55%**

- **Confusion Matrix**:

  |                     | Predicted: No | Predicted: Yes |
  |---------------------|---------------|----------------|
  | **Actual: No**      | 1515          | 80             |
  | **Actual: Yes**     | 200           | 205            |
- **Accuracy**: **86%**

- **Single Prediction**:
  - Input: `[France, 600, Male, 40, 3, 60000, 2, Yes, Yes, 50000]`
  - Prediction: **No** (the customer will not leave the bank).