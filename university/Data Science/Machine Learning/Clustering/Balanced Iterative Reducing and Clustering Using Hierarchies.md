---
uni-module: "KDD"

alias: "BIRCH"
---

# Balanced Iterative Reducing and Clustering Using Hierarchies

A [[Hierarchical Clustering]] method which uses the following two phases:

- Phase 1: Builld an inital [[CF-Tree]] ([[Clustering Feature]]) which is a multi-level compression of the data that preserves inherent clustering structure of the data
- Phase 2: Use any [[Clustering]] method to cluster the leaf nodes of the CF-Tree

## Algorithm

1. For each point
   1. Find closest leaf-node entry
   2. Add point to leaf-node entry and update [[Clustering Feature|CF]]
   3. If entry_diameter > max_diameter, then split leaf node and possibly parents
   4. Information about new point is passed to root

[[Laufzeit]] is $\mathcal{O}(n)$ and incremental.

## Advantages

- Finds good clustering with a single scan
- Can finetune the clustering with additional scans

## Disadvantages

- **BUT** only handles numeric data and is quite sensitive to the order of the data records
- Sensitive to insertion order of data points
- [[Cluster|Clusters]] may not be natural as we fix the size of the leaf nodes
- [[Cluster|Clusters]] tend to be spherical given the radius and diameter measures
