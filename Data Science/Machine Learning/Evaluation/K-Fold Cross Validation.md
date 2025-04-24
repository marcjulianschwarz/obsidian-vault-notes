---
uni-module: "KDD"
---
# K-Fold Cross Validation

1. shuffle data
2. split data in $k$ folds (with each having approximately the same size)
3. for each foldc(so $k$ times)
   1. use the fold as validation set
   2. use the rest to train the model
   3. train the model
   4. evaluate the model on the validation set → [[Performance Evaluation Metrics]]
4. Take the average of all folds

This procedure ensures that your model has been validated on every [[Entity|sample]] of your [[Dataset]] and not only on a simple 30-70 split.

A good value for $k$ is 10 (empirical analysis).

For very small data sets use [[Leave-One-Out K-Fold Cross Validation]].

## Example

![[Bildschirmfoto 2022-10-09 um 19.24.49.png]]
