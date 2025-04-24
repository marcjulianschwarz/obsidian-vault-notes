---
uni-module: "KDD"

alias: "LOOCV"
---
# Leave-One-Out K-Fold Cross Validation

Basically [[K-Fold Cross Validation]] but with $k=N$ folds.

This is computationally really expensive and should thus only be used on really small datasets where it is very important that the model has been tested on all of the data.
