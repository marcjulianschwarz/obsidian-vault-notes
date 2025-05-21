---
uni-module: "KDD"
---

# Outlier Detection with Grouping Based on Assumptions

We can group data based on some assumptions on the data.

## Statistical Methods

With the statistical model we assume that the _normal_ data followes some statistical model or stochastic process ([[Wahrscheinlichkeitsmaß|Distribution]]) and that all data that is not following this model is an [[Outlier]].
The idea is to fit a generative model to the data set and identiy outliers in the low-probability regions of the model (for example left and right tails in [[Normalverteilung|Normal Distribution]])
We can for example use a [[Normalverteilung|Gaussian Distribution]] to model the normal data and then calculate the probability of outliers with this model which is going to be very low.

The effectiveness of this method highly depends on whether the statistical model is actually describing the underlying random mechanism of the real data.

[[Outlier Detection with Parametric Statistical Method]]

## Proximity-Based Methods

An object is an outlier if the nearest neighbors of the object are far away.
There are two major types of proximity-based outlier detection:

- distance-based
- density-based

### Some Challenges

- highly relies on the [[Proximity]] measure
- in some applications, proximity cannot be obtained easily
- difficult to find outliers in a group of outliers which are all close to each other

## Clustering-Based Methods

Similar to [[Outlier Detection with Outlier Classification]] with [[Unsupervised Learning]].

Normal data belongs to a large and dense cluster whereas outliers belong to small and [[Sparsity|sparse]] clusters or do not belong to any [[Cluster]] at all.

Many [[Clustering]] methods can be used, however most clustering algorithms are quite costly and don't scale well for large datasets.
