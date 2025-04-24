---
uni-module: "KDD"

alias: "Bootstrapped Optimistic Algorithm for Tree Construction"
---

# BOAT

[[Decision Tree Induction]] algorithm that is scalable.

Uses [[Bootstap|Bootstraping]] to create several smaller [[Sample|samples]] each fitting in memory. Each subset will be used to create a tree which will then be combined into the final [[Decision Tree]].

## Advantages

- scalable → [[Datenbank|Database]] only needs to be scanned twice
- incremental → can be update with new data
