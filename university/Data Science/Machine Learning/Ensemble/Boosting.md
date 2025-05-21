---
uni-module: "KDD"
---

# Boosting

An [[Ensemble Method]] that is quite similar to the [[Bagging]] method.

> [!TIP] Analogy
> Diagnosis based on multiple doctors where each diagnosis gets a weight assigned to it based on the previous diagnosis [[Accuracy]].

Each training tuple will get a weight assigned to it and a series of [[Classification|classifiers]] will be trained iteratively on a partition of the dataset that will be created using the [[Bootstap]] method with the associated weights. However after each trained classifier the weights will be updated to allow the subsequent classifiers to pay more attention to the missclassified tuples.
This means missclassified tuples will be weighted more than correctly classified tuples.

The final _boosted_ classifier combines the votes of each individual classifier where each vote will be weighted by the accuracy of the classifier.
The class with the most votes will be assigned to the sample.

Of course this method can also be extended to [[Regression]].

One example of boosting is [[AdaBoost]].
