---
uni-module: "AI"

tags: Algorithmus
---

# Cutset Conditioning Algorithm

Computes an optimal [[Cutset]] for a [[Constraint Satisfaction Problem|CSP]] and an existing [[Cutset]] $V_{0}$.

## Pseudocode

![[Bildschirm­foto 2022-12-11 um 15.29.30.png]]

## [[Laufzeit|Running Time]]

The algorithm is [[Exponential Growth|exponential]] only in the number of nodes in $V_{0}$ not in $V$.

However finding optimal cutsets is [[Nondeterministic Polynomial Time Complete|NP-hard]]. There exist approximations which can be solved easier.
