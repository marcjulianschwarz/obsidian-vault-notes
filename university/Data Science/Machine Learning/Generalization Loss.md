---
uni-module: AI
---
# Generalization Loss

The generalization loss for a hypothesis $h$ from a given [[Hypothesis Space]] with respect to a [[Loss Function]] $L$ and examples $\mathcal{E}$ is 
$$\operatorname{GenLoss}_L(h):=\sum_{(x, y) \in \mathcal{E}} L(y, h(x)) \cdot P(x, y).$$
We can find the best hypothesis 
$$h^*:=\underset{h \in \mathcal{H}}{\operatorname{argmin}} \operatorname{GenLoss}_L(h).$$

As $P(X, Y)$ is unclear in practice we can only estimate the loss with the [[Empirical Loss]].