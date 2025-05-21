---
uni-module: "AI"
---

# Description Logic

A [[Formal System]] for talking about **collections** of objects and their relations.
It is at least as [[Expressive Adequacy|expressive]] as [[Propositional Logic]] with set-theoretic semantics, and it offers

- individuals
- relations

It has the following components.

- a formal language $\mathcal{L}$ with [[Logical Constant|logical constants]] $\sqcap, \bar{\circ}, \sqcup, \sqsubseteq, \equiv$
- a set-theoretic semantics $\langle \mathcal{D}, [[\circ]] \rangle$
  - we get this for free when we can translate into [[First-Order Predicate Logic]]
- [[Translation into First-Order Predicate Logic]] that is compatible with the set-theoretic semantics
- a [[Inference Rule|Calculus]] for $\mathcal{L}$ that includes a decision procedure for $\mathcal{L}$ satisfiability
  - to verify we are still in the decidable region of logics

[[Assertion|ABox]]

[[Closed World Assumption]] vs. [[Open World Assumption]]

## TBoxes

[[Terminology|TBox]]
[[Concept Definition]]
