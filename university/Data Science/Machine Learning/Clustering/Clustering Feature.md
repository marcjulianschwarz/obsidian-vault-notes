---
uni-module: "KDD"

alias: "CF"
---

# Clustering Feature

Part of a CF-Tree which is used in the [[Balanced Iterative Reducing and Clustering Using Hierarchies|BIRCH]] algorithm.

It is a 3D summarizing statistic about the current [[Cluster|Clusters]].

$$CF=(n,LS,SS)$$
where $n$ is the number of data points in the cluster, $LS$ is the linear sum of the points in the cluster and $SS$ is the square sum of the points in the cluster.

This statistic allows to derive some useful information about a cluster.

Centroid:
$$\frac{LS}{n}$$
Radius:
$$\sqrt{ \frac{nSS-2LS^2+n}{n^2} }$$
Diameter:
$$\sqrt{ \frac{2nSS-2LS^2}{n(n-1)} }$$

A nice way of **merging** two clusters is to just add the two CFs of two clusters.

## Example

![[Bildschirmfoto 2022-10-02 um 17.44.27.png]]
