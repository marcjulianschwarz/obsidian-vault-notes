---
uni-module: "AI"
---

# Partially Ordered Plan

Let there be a [[STRIPS Task]]. Then a partially ordered plan is a labeled [[Directed Acyclic Graph|DAG]]:

- nodes (steps) are labeled with [[Action|actions]]
  - [[Start Step]]
  - [[Finish Step]]
- [[Causal Link]]

[[Temporal Constraint]]

We want to have no [[Open Condition|open conditions]] in the end.

[[Possibly Intervening Step]]

A [[Partially Ordered Plan]] is complete iff every [[Precondition]] is achieved.
