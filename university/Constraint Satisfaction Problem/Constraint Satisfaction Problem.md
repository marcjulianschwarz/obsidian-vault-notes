---
uni-module: "AI"

alias: ["CSP", "Constraint Network"]
---

# Constraint Satisfaction Problem

Consists of:
- variables
- their domains
- and constraints between variables

Can be visualized in a [[Constraint Graph]] and solved using the [[Backtracking Search]] algorithm.

We can use [[Inference]] in [[Constraint Satisfaction Problem|CSPs]] to more or less _prune_ the problem before solving it (constraint propagation). It works by adding new constraints that follow from the already known constraints.

Two examples of this method are:
- Forward Checking
- Arc Consistency


- Equivalence
- Tightness
- Waltz Algorithm

## Decomposition: Constraint Graphs, and Three Simple Cases


- Decomposition
- Constraint Propagation with Local Search 
- [[Cutset]]
- [[Cutset Conditioning Algorithm]]
