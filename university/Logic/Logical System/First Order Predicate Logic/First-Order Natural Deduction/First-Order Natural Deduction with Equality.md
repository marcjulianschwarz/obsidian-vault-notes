---
uni-module: "AI"
---

# First-Order Natural Deduction with Equality

An extension of the [[First-Order Natural Deduction]] [[Inference Rule|Calculus]] to support the equality predicate of the [[First-Order Predicate Logic with Equality]], called $\mathcal{ND}^1_=$.
We add the following rules:
![[Bildschirm­foto 2023-01-31 um 11.22.54.png]]

Where $C[A]_p$ is the formula $C$ which has a subterm $A$ at the position $p$. This basically means if $A=B$ we can replace all $A$s in $C$ with $B$s.

You can think of the postition $p$ as a position in a tree of $C$, which might look like this schematically:

![[Bildschirm­foto 2023-01-31 um 11.26.37.png]]

In lots of ways equivalence behaves like equality in a logical way. Thats why we add the following additional rules for equivalence:

![[Bildschirm­foto 2023-01-31 um 11.25.28.png]]
