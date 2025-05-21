---
uni-module: AI
aliases:
  - Error Function
---
# Loss function

$$L(x, y, \widehat{y})$$
The amount of utility lost py predicting $\hat{y}$ instead of $y$. We can often also use 
$$L(y, \hat{y})$$ when the loss is independent of $x$.

- [[Generalization Loss]]
- [[Empirical Loss]]

A [[Deep Learning]] model can improve by changing the weights and biases values. To do this, the model needs to know how good it performs and therefore we need a metric that can measure this performance. Depending on the type of problem we want to solve with our [[Deep Neural Network|DNN]] one of the following metrics might be a solution:

- Regression: [[Mean Squared Error]]
- Classification: [[Cross Entropy]]
- [[Cross Entropy]]

