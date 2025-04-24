---
uni-module: KDD
related:
  - "[[Underfitting]]"
---
# Overfitting

When a trained model describes random error in the training set rather than the underlying relationship. This leads to low [[Bias]] on the training set but high [[Varianz|Variance]] on the test set.

Generally overfitting increases with the size of the [[Hypothesis Space]] and number of attributes, but decreases with the number of examples.

## Prevention 

- [[Decision Tree Pruning]]
- [[Ridge Regression]]
- [[Lasso Regression]]
- increase training set size 
- decrease [[Hypothesis Space]] (e.g. by choosing simpler model)



