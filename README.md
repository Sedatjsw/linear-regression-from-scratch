# Linear Regression from Scratch using the Normal Equation

This project demonstrates the implementation of Linear Regression from scratch using the Normal Equation and NumPy, without relying on machine learning libraries such as scikit-learn.

The project focuses on understanding the mathematical foundations of linear regression, numerical computation, model evaluation, and computational scaling behaviour.

---

## Project Overview

The main objective of this project is to build and evaluate a simple linear regression model using matrix algebra and numerical computing techniques.

The implementation uses the Normal Equation to estimate regression coefficients directly from the data.

The project also investigates how the computational cost of the Normal Equation changes as dataset size and feature dimensionality increase.

---

## Key Concepts Demonstrated

* Linear Regression
* Normal Equation
* Matrix Algebra
* Numerical Computing
* Regression from Scratch
* Model Evaluation
* Computational Complexity
* Scaling Analysis

---

## Technologies Used

* Python
* NumPy
* Pandas
* Matplotlib

---

## Dataset

The project uses a real-world housing dataset containing approximately 1000 observations.

### Variables

* Feature: `Square_Footage`
* Target: `House_Price`

The relationship between house size and price is modelled using a single-feature linear regression model:

```text id="k3d8rp"
y = aX + b
```

---

## Model Implementation

The regression model was implemented manually using the Normal Equation:

```text id="x5m9qw"
β = (XᵀX)⁻¹ Xᵀy
```

For improved numerical stability, the implementation uses:

```text id="n0v7kl"
np.linalg.solve(X.T @ X, X.T @ y)
```

instead of explicitly computing the matrix inverse.

No machine learning libraries were used during model implementation.

---

## Workflow

### Data Preparation

* Feature and target extraction
* Train/test split
* Matrix construction for regression

### Model Training

* Computation of regression coefficients using matrix operations
* Estimation of slope and intercept values

### Prediction

* Generation of predicted house prices using the fitted regression line

### Evaluation

Model performance was evaluated using:

* RMSE (Root Mean Squared Error)
* Train/test evaluation

---

## Results

The model successfully captured the primary linear relationship between house size and house price.

### Key Results

* Slope ≈ 200
* Intercept ≈ 55,000
* RMSE ≈ 33,431
* Relative error ≈ 5.4%

The regression line explained the overall trend effectively, although some variability remained due to factors not included in the model.

---

## Computational Scaling Analysis

The project also explored the computational behaviour of the Normal Equation under different dataset sizes and feature dimensions.

### Observations

* Runtime increased slowly as the number of samples increased
* Runtime increased much more rapidly as the number of features increased
* Computational cost depended primarily on feature dimensionality

The analysis demonstrated one of the key limitations of the Normal Equation:

* It performs well for small feature spaces
* It becomes computationally expensive for high-dimensional datasets

---

## Technical Report

A presentation-style technical report containing:

* Model implementation details
* Performance evaluation
* Scaling analysis
* Visualisations
* Interpretation of results

is included in the `reports` folder.

---

## Project Structure

```text id="w8p2zm"
linear-regression-from-scratch
 ├── data
 ├── notebooks
 ├── reports
 └── README.md
```

---

## Skills Demonstrated

* Machine Learning Fundamentals
* Linear Regression
* Matrix Operations
* Numerical Computing
* Model Evaluation
* Data Analysis
* Python Programming
* Computational Analysis

---

## Conclusion

This project demonstrates the mathematical and computational foundations of Linear Regression using the Normal Equation.

The implementation highlights both the strengths and limitations of analytical regression methods, while also providing insight into numerical stability and computational scaling behaviour.

---

## Author

Sedat Aydin
MSc Big Data Analytics & Artificial Intelligence
