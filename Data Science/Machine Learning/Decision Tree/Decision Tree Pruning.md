---
uni-module: KDD
aliases:
  - Tree Pruning
---
# Decision Tree Pruning

Method to avoid [[Overfitting]] for [[Decision Tree]] when there are too many branches that might even reflect [[Outlier]] or noise.

Pruned trees are smaller, faster, less complex and better at classifying unseen data.

## Prepruning

Halt [[Decision Tree Induction]] early if _goodness_ measure falls below a threshold.

## Postpruning

Progressively remove terminal nodes from an overfit tree and use testset or [[Information Gain]] to decide which is the best pruned tree. 

