# Gradient Descent in Linear Regression

## Overview
Gradient descent is an optimization algorithm used to iteratively minimize a loss function by adjusting the model's parameters (weights and bias). It plays a crucial role in linear regression by finding the parameters that produce the model with the lowest possible loss.

## Key Concepts

### **Steps of Gradient Descent**
1. **Initialize weights and bias:**
   - Begin with random values near zero for weights and bias.

2. **Iterative updates:**
   - **Calculate loss:** Compute the loss using the current weights and bias.
   - **Determine gradient direction:** Identify the direction that reduces the loss.
   - **Update parameters:** Move the weights and bias a small step in the direction of reduced loss.

3. **Repeat until convergence:**
   - Continue updating weights and bias until loss stabilizes and cannot be further reduced significantly.

---

### **Illustrative Example**
Using a small dataset:

| Pounds (1000s) | Miles per Gallon |
|----------------|-------------------|
| 3.5            | 18                |
| 3.69           | 15                |
| 3.44           | 18                |
| 3.43           | 16                |
| 4.34           | 15                |
| 4.42           | 14                |
| 2.37           | 24                |

1. **Initial Parameters:** Start with weight = 0 and bias = 0.
2. **Iterative Updates:**

| Iteration | Weight | Bias  | Loss (MSE) |
|-----------|--------|-------|------------|
| 1         | 0      | 0     | 303.71     |
| 2         | 1.2    | 0.34  | 170.67     |
| 3         | 2.75   | 0.59  | 67.3       |
| 4         | 3.17   | 0.72  | 50.63      |
| 5         | 3.47   | 0.82  | 42.1       |
| 6         | 3.68   | 0.9   | 37.74      |

Loss decreases with each iteration until the model converges.

---

### **Loss Curve**

The loss curve shows how loss evolves during training:
- **Steep decline:** Early iterations rapidly decrease the loss.
- **Gradual decline:** Subsequent iterations slowly reduce loss.
- **Convergence:** Loss stabilizes, indicating the model has found the optimal weights and bias.

---

## Model Convergence

1. **Definition:**
   - A model converges when further iterations do not significantly reduce loss.

2. **Convex Loss Function:**
   - For linear models, the loss function creates a convex surface, ensuring gradient descent always finds the global minimum.

3. **Loss Surface Visualization:**
   - Example:
     - Weight = -5.44
     - Bias = 35.94
     - Minimum Loss = 5.54

Gradient descent moves parameters along the loss surface, resembling a ball rolling downhill until it stops at the lowest point.

---

## Key Terminology

- **Convergence:** State where further iterations do not reduce loss.
- **Convex Function:** A shape that guarantees the global minimum for linear models.
- **Gradient Descent:** Iterative algorithm to minimize the loss function.
- **Iteration:** Single step of updating weights and bias.
- **Loss Curve:** Graph showing how loss changes during training.

---

## Key Takeaways

1. Gradient descent optimizes the weights and bias to minimize loss.
2. Convergence occurs when loss stabilizes, indicating the optimal parameters.
3. Linear regression benefits from convex loss functions, ensuring reliable optimization.
4. Loss curves help monitor model progress and identify convergence.
5. Gradient descent seldom finds the exact minimum but approximates closely.

---

For further details, explore:
- [Linear Regression Basics](#)
- [Hyperparameter Tuning](#)
- [Advanced Optimization Techniques](#).

