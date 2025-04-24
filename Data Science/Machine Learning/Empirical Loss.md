---
uni-module: AI
---
# Empirical Loss

An estimation of the [[Generalization Loss]] given a [[Loss Function]] $L$ and set $E$ with a total of $N$ examples. 

$$\operatorname{EmpLoss}_{L, E}(h):=\frac{1}{N}\left(\sum_{(x, y) \in E} L(y, h(x))\right)$$
We then get the estimated best hypothesis 
$$\widehat{h}^*:=\underset{h \in \mathcal{H}}{\operatorname{argmin}} \text { EmpLoss }_{L, E}(h)$$
