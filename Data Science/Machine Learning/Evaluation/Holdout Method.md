---
uni-module: KDD
aliases:
  - Holdout Cross Validation
---
# Holdout Method

Split dataset into **training set**, **validation set** and **test set** based on a simple fraction (e.g. 70-20-10).

The estimates from this method are highly dependent on the partioning of the data.

We can thus use random sampling to repeat the holdout method $k$ times and create an average over a lot of partitions, this is called [[K-Fold Cross Validation]].

- [[Leave-One-Out K-Fold Cross Validation]]
