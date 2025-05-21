---
uni-module: "AI"

alias: ["mgu", "MGU"]
---

# Most General Unifier

A substitution is called a **most general** unifier when it is [[More General]] than all other unifiers.
Which means it is minimal in the [[Unification]] problem solutions with respect to the [[More General]] definition on all free variables of $A$ and $B$.

Every pair of $A$ and $B$ has a most general unifier or it doesnt have one at all. And it can be computed in linear time.
