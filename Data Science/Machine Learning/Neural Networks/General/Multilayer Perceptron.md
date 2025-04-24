---
uni-module: ML4ENG
---

# Multilayer Perceptron

To create more complex models, we can combine multiple [[Perceptron|perceptrons]], all with their own set of weights and biases.

The outputs of a layer can be calculated with this formula, where the input values get a weight with $W$, a bias value $b$ is added and the [[Logistic Function|Sigmoid]] [[Activation Function]] will be applied to the resulting value.
$$y = \sigma(W \cdot x + b)$$
By combining multiple layers, using the outputs of former layers as new inputs, the following recursive formula applies:
$$y^{i+1} = \sigma(W^i \cdot y^i + b^i)$$
