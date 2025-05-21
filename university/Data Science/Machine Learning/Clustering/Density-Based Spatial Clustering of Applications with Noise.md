---
uni-module: "KDD"

alias: "DBSCAN"
---

# Density-Based Spatial Clustering of Applications with Noise

A [[Density-Based Clustering]] method which can detect [[Cluster|Clusters]] of arbitrary shape in spatial databases with noise.

Basic Algorithm:

1. Mark all objects as unvisited
2. Randomly select unvisited object $p$ and mark it as visited
3. If $p$ is no [[Core Point]] mark it as noise
4. Else, create new cluster $C$ for point $p$
5. Add all objects from the $\epsilon$ neighborhood of $p$ to the candidate set $N$
6. For each $n$ in $N$ that does not yet belong to a cluster
   1. Add $n$ to cluster $C$
   2. Mark $n$ as visited
   3. If $n$ is [[Core Point]], add all objects from the $\epsilon$ neighborhood to $N$
7. Ends when $N$ is empty, so $C$ cant be expanded
8. Continue process until all points have been visited

## Disadvantages

- sensitive to choice of parameters (see image)

![[Bildschirmfoto 2022-10-10 um 18.41.17.png]]
