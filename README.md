# Linear Regression From Scratch Using NumPy

## 1. Project Overview

This project implements Simple Linear Regression and Multiple Linear Regression from scratch using Python and NumPy.

The California Housing dataset is used to predict house prices based on different housing-related features.

The main objective is to understand how Linear Regression works internally without depending on Scikit-learn for model training.

## 2. Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Google Colab

## 3. Dataset

The California Housing dataset is used in this project.

- Total records: 20,640
- Input features: 8
- Target variable: Median House Value
- Training data: 80%
- Testing data: 20%

The dataset is divided into training and testing sets using `train_test_split`.

Feature standardization is performed using the training dataset's mean and standard deviation.

## 4. Mathematical Implementation

### Hypothesis Function

The model predicts the output using:

h(X) = Xθ

Where:
- X represents the input features.
- θ represents the model parameters.
- h(X) represents the predicted values.

### Cost Function

The training cost function is:

J(θ) = 1/(2m) × Σ(h(xᵢ) − yᵢ)²

Where:
- m is the number of training examples.
- h(xᵢ) is the predicted value.
- yᵢ is the actual value.

### Gradient Descent

The gradient descent update rule is:

θ = θ − α × (1/m) Xᵀ(Xθ − y)

Where:
- α is the learning rate.
- θ represents the model parameters.

Gradient Descent updates the parameters repeatedly to minimize the cost.

## 5. Implementation

The project includes:

1. Simple Linear Regression using one feature (`MedInc`).
2. Multiple Linear Regression using all eight features.
3. Hypothesis function implemented using NumPy.
4. Cost function implemented using NumPy.
5. Gradient Descent using matrix operations.
6. Feature standardization.
7. Cost convergence visualization.
8. Manual calculation of MSE and R².
9. Comparison with Scikit-learn Linear Regression.

## 6. Model Evaluation Results

| Model | Features | Test MSE | Test R² |
|---|---:|---:|---:|
| Simple Linear Regression | 1 | 0.709116 | 0.458859 |
| Multiple Linear Regression (From Scratch) | 8 | 0.555903 | 0.575779 |
| Multiple Linear Regression (Scikit-learn) | 8 | 0.555892 | 0.575788 |

## 7. Result Analysis

- Multiple Linear Regression performed better than Simple Linear Regression.
- The multiple regression model achieved a test R² score of approximately 0.576.
- The NumPy implementation produced results very close to Scikit-learn.
- The small difference in results is due to the optimization methods used.

## 8. Conclusion

Linear Regression was successfully implemented from scratch using NumPy.

Both Simple and Multiple Linear Regression were trained and evaluated using the California Housing dataset.

The results demonstrate that the manually implemented Multiple Linear Regression model performs nearly as well as the Scikit-learn implementation.

## 9. How to Run

1. Open the notebook in Google Colab.
2. Run the cells sequentially.
3. Load the California Housing dataset.
4. Train the regression models.
5. View the convergence graphs and evaluation results.
