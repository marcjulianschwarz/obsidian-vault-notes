---
uni-module: "KDD"
---

# Random Forest

An [[Ensemble Method]] consisting only of [[Decision Tree|decision trees]] where each tree has been generated using **random** attribute selections at each node.

Each tree will give a vote and the class with the most votes will be assigned to the sample.

There are two major methods to construct random forests:

- [[Forest-RI]]
- [[Forest-RC]]

Random Forests are comparable in [[Accuracy]] to [[AdaBoost]] but are more robust to errors and [[Outlier|Outliers]].
Also they are faster than most or all [[Bagging]] and [[Boosting]] methods.
