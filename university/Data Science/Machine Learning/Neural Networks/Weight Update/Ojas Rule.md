
# Oja’s Rule

Oja’s rule is a modification of the Hebbian Learning rule and could be seen as its constrained form, which ensures that the norm (length) of the weight vector doesn't grow uncontrollably.

> Cells that fire together, wire together.

Consider a single-layer linear neuron that gets an input vector $X$, has weight vector $W$, and produces an output $y$. The neuron's output, $y$, is a weighted sum of its inputs:
$$
y = W^T X
$$
Then, the weights are updated as per Oja's rule:
$$
\Delta W = \eta y (X - yW)
$$
Where:
- $\eta$ is the learning rate, a parameter that decides how much an update impacts the weights.
- $X - yW$ is used to keep the weights bounded, essentially subtracting the projection of the weight vector on the input vector from the input vector itself.

The intuition behind this rule is that it allows a neuron to learn to represent the highest variance directions in the input data with its strongest connections ($W$), effectively performing [[Principle Component Analysis|PCA]].

