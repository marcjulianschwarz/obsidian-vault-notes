---
uni-module: AI
aliases:
  - Regularization
---
# Regularisation

Having a big [[Hypothesis Space]] can lead to [[Overfitting]]. To reduce this overfitting we can try to penalize a hypothesis that is too complex by adding its complexity to the [[Empirical Loss]] and therefore increasing the **total cost** of it. 

$$\operatorname{Cost}_{L, E}(\boldsymbol{h}):=\operatorname{EmpLoss}_{L, E}(\boldsymbol{h})+\lambda \operatorname{Complexity}(\boldsymbol{h})$$

Minimizing this regularized version of the [[Empirical Loss]]

$$\widehat{h}^*:=\underset{h \in \mathcal{H}}{\operatorname{argmin}} \operatorname{Cost}_{L, E}(\boldsymbol{h})$$

is called regularization. 
We can use the parameter $\lambda$ to control how much influence the regularization should have. 

[[Minimum Description Length]]

**Methods:**
- [[Lasso Regression]]
- [[Ridge Regression]]
- [[Elastic-Net Regression]]
- [[Dropout]]
- [[Early Stopping]]
- [[Square Weight Decay]]

![[Bildschirmfoto 2023-07-26 um 11.16.47.png]]

![[Bildschirmfoto 2023-07-26 um 11.18.05.png]]