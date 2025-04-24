---
uni-module: "KDD"

alias: "Clustering Feature Tree"
---
# CF-Tree

A [[Height-Balanced Tree]] which stores the [[Clustering Feature|clustering features]] for a [[Hierarchical Clustering]] based on the [[Balanced Iterative Reducing and Clustering Using Hierarchies|BIRCH]] algorithm.

In it all non-leaf nodes store the sums of the CFs of all their children.

It has two parameters that limit the tree:

- $B$ , the branching factor is the max number of children
- $T$, the threshold is the max diameter of sub-clusters stored at leaf nodes

## Example

![[Bildschirmfoto 2022-10-02 um 18.01.39.png]]
