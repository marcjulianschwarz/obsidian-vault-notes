---
uni-module: "KDD"

alias: "AGNES"
---

# Agglomerative Nesting

AGNES is a [[Hierarchical Clustering]] method which uses the _sinlge-link method_ to merge datapoints with the least [[Dissimilarity]].

Evenutally all nodes belong to the same [[Cluster]], thus a stopping condition has to be specified.

This method can be thought of like a [[Dendogram]] where we can get any desired clustering resolution by **cutting** the dendogram at a certain level where then each connected component forms a cluster.

![[Bildschirmfoto 2022-10-02 um 17.28.48.png]]

## Disadvantages

- Cant undo what was done previously
- [[Laufzeit]] of $\mathcal{O}(n^2)$
