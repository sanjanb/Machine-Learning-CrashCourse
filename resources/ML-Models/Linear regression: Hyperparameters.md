# Linear Regression: Hyperparameters

## Introduction
Hyperparameters are external configurations that control different aspects of a machine learning model's training process. Unlike parameters (e.g., weights and biases) that the model learns during training, hyperparameters are set before training begins and directly influence the training efficiency and model performance.

### Common Hyperparameters
1. **Learning Rate**
2. **Batch Size**
3. **Epochs**

---

## Learning Rate
The **learning rate** is a floating-point number that determines the size of the steps taken during the optimization process. It controls how quickly or slowly a model converges to the minimum of the loss function.

### Characteristics:
- **Too low:** Training becomes excessively slow, as the model takes small steps.
- **Too high:** The model fails to converge, oscillating around or diverging from the optimal solution.
- **Optimal:** Achieves convergence in a reasonable number of iterations.

### Calculation:
During gradient descent, the model updates parameters as follows:

\[ \text{New Parameter} = \text{Old Parameter} - (\text{Learning Rate} \times \text{Gradient}) \]

For example, if the gradient's magnitude is 2.5 and the learning rate is 0.01, the parameter update is:
\[ 2.5 \times 0.01 = 0.025 \]

### Visualizing Learning Rates:
- **Optimal:** Loss decreases significantly during the initial iterations and stabilizes (Figure 21).
- **Too Low:** Loss decreases very slowly (Figure 22).
- **Too High:** Loss fluctuates wildly or increases over time (Figures 23 & 24).

---

## Batch Size
The **batch size** determines the number of training examples processed before updating the model's parameters. 

### Types:
1. **Full-Batch Gradient Descent:** Uses the entire dataset per iteration.
   - Pros: Accurate gradient calculation.
   - Cons: Computationally expensive for large datasets.

2. **Stochastic Gradient Descent (SGD):** Uses a single example per iteration.
   - Pros: Less computational cost per iteration.
   - Cons: High noise in parameter updates.

3. **Mini-Batch Gradient Descent:** Processes a subset of the dataset per iteration.
   - Pros: Balances computational efficiency and gradient accuracy.
   - Cons: Requires selecting an appropriate batch size.

### Behavior:
- **Small Batch Sizes:** Introduce noise but help generalization.
- **Large Batch Sizes:** Resemble full-batch behavior, with less noise but higher computational requirements.

---

## Epochs
An **epoch** represents one complete pass through the entire training dataset.

### Characteristics:
- **More Epochs:** Often improve model performance but increase training time.
- **Fewer Epochs:** May result in underfitting, where the model fails to learn sufficiently.

### Relation to Iterations:
The number of parameter updates depends on the batch size and the number of epochs:

- **Full Batch:** Updates once per epoch.
- **SGD:** Updates for every example in the dataset.
- **Mini-Batch:** Updates for each batch in the dataset.

### Example:
- Dataset size: 1,000 examples.
- Batch size: 100 examples.
- Epochs: 20.

| Batch Type | Updates per Epoch | Total Updates (20 Epochs) |
|------------|-------------------|--------------------------|
| Full Batch | 1                 | 20                       |
| SGD        | 1,000             | 20,000                   |
| Mini-Batch | 10                | 200                      |

---

## Key Takeaways
- **Hyperparameters** like learning rate, batch size, and epochs significantly affect the training process and model performance.
- **Learning rate:** Affects the speed and stability of convergence.
- **Batch size:** Balances computational efficiency and generalization.
- **Epochs:** Determines how thoroughly the model learns from the dataset.

---

## Glossary
- **Batch Size:** Number of examples processed before parameter updates.
- **Epoch:** Complete pass through the training dataset.
- **Gradient Descent:** Optimization algorithm used to minimize the loss function.
- **Learning Rate:** Magnitude of parameter updates during training.
- **Mini-Batch:** Subset of data used in mini-batch gradient descent.
- **Parameter:** Variables like weights and biases, learned by the model.
- **Stochastic Gradient Descent:** Gradient descent with a batch size of 1.
