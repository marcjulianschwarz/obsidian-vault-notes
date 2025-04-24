---
uni-module: "KDD"
---

# Partition-Based Clustering

The overall strategy here is to partition the [[Dataset]] into a set of $k$ clusters $C_{i}$ such that the sum of squared distances to $c_{i}$ is minimized, where $c_{i}$ is the centroid or medoid of a cluster $C_{i}$.
$$\min \sum_{i=1}^k (\sum_{j=1}^n d\left(o_j, c_i\right)^2$$
You could enumerate all possible partitions and therefore find the optimal solution or you could use [[Heuristik|heuristic]] methods like:

- [[k-means Clustering]]
- [[k-medoids Clustering]]
- [[Clustering Large Applications]]
- [[Randomized CLARA]]
