# Linear Regression: Loss

## Overview
Loss is a numerical metric that quantifies how incorrect a model's predictions are. It measures the distance between the model's predictions and the actual labels. The primary goal of training a model is to minimize loss, effectively improving its accuracy.

In linear regression, loss can be visualized as arrows drawn from the data points to the model. These arrows represent the error or distance between the predicted and actual values.

---

## Key Concepts

### Definition of Loss
Loss measures the difference between the predicted values and actual values, focusing on the magnitude of the error rather than its direction. For instance:
- If a model predicts `2` but the actual value is `5`, the focus is on the distance `|5 - 2| = 3`, not whether the error is positive or negative.

### Removing the Sign of Errors
To handle errors, the sign is removed using:
1. **Absolute Value**: Taking the absolute difference.
2. **Squaring**: Squaring the difference.

### Types of Loss
There are four primary types of loss in linear regression:

| Loss Type        | Definition                                                                             | Equation |
|------------------|-----------------------------------------------------------------------------------------|----------|
| **L1 Loss**      | The sum of the absolute differences between the predicted and actual values.           |          |
| **MAE**          | The average of L1 losses across all examples.                                          |          |
| **L2 Loss**      | The sum of squared differences between the predicted and actual values.                |          |
| **MSE**          | The average of L2 losses across all examples.                                          |          |

The key difference between L1 and L2 loss lies in the squaring. Squaring emphasizes larger errors, making L2 loss more sensitive to outliers than L1 loss.

---

## Choosing a Loss Function
When deciding between Mean Absolute Error (MAE) and Mean Squared Error (MSE), consider:
- **MAE**: Less sensitive to outliers.
- **MSE**: Penalizes larger errors more heavily, moving the model closer to outliers.

For example:
- A model trained with MSE will tilt toward outliers.
- A model trained with MAE will maintain a distance from outliers but align closely with most data points.

### Visualizing Loss Functions
- **MSE**: The model aligns closer to outliers.
- **MAE**: The model remains further from outliers but closer to the majority of data.

---

## Example: Calculating Loss
Given a model with the following values:
- Predicted value: `21.5 mpg`
- Actual value: `24 mpg`

To calculate the L2 loss for a single data point:

\[
L2 = (24 - 21.5)^2 = 6.25
\]

The L2 loss for this single example is `6.25`.

---

## Understanding Outliers
Outliers can affect the choice of a loss function. For instance:
- **Typical Range**: Cars weighing 2000–5000 pounds and getting 8–50 mpg.
- **Outliers**: Cars outside this range or those with extreme deviations in predictions.

**Impact on Loss Functions**:
- **MSE**: Penalizes outliers heavily, causing the model to move closer to them.
- **MAE**: Less influenced by outliers, keeping the model aligned with the majority of data.

---

## Key Takeaways
- Loss quantifies the error in a model's predictions.
- Training a model involves minimizing the loss.
- MAE and MSE are common loss functions with distinct characteristics:
  - **MAE**: Robust to outliers.
  - **MSE**: Sensitive to outliers, penalizing larger errors more heavily.

---

## Glossary
- **Loss**: A measure of prediction error.
- **L1 Loss**: Sum of absolute errors.
- **L2 Loss**: Sum of squared errors.
- **MAE (Mean Absolute Error)**: Average of L1 losses.
- **MSE (Mean Squared Error)**: Average of L2 losses.
- **Outlier**: Data point significantly deviating from the norm.
- **Prediction**: The model's estimated value.

---

### Further Reading
- [Linear Regression Basics](#)
- [Advanced Loss Functions](#)

---

**License:** This content is licensed under the Creative Commons Attribution 4.0 License. Code samples are licensed under the Apache 2.0 License.
