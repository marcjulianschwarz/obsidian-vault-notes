---
uni-module: "AI"
---

# Unification Algorithm

A [[Inference Rule|Calculus]] $\mathcal{U}$ to solve the [[Unification Problem]] with the following rules:

Decomposition Rule, Trivial Rule, Elimination Rule.

![[Bildschirm­foto 2023-01-31 um 13.10.56.png]]

Elimination Rule is kind of like Constraint Propagation.

This algorithm is

- correct
- [[Completeness|complete]]
- correct + complete → the [[Most General Unifier|MGU]] of all derived forms (including the [[Solved Form]]) is the same as the problem in the beginning
- [[Confluent]]
  - there can only be one [[Most General Unifier|MGU]]

→ this is **unitary**, so [[Most General Unifier|MGU]]s are unique

We are doing tightenens that are equivalent.

Correctness and [[Completeness]] ←→ Tightness and Equivalence in [[Constraint Satisfaction Problem|CSP]]
