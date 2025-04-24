---
uni-module: "AI"
---

# Concept Definition

Let $\mathcal{D}$ be a [[Description Logic]] with concepts $\mathcal{C}$.

We can define a new [[Concept]] with a pair $c=C$ where $c$ is a new concept and $C\in \mathcal{C}$ is a $\mathcal{D}$ formula.

We can for example define a mother as $\text{mother} = \text{woman} \sqcap \text{has child}$.

A concept definition is **recursive** when the new concept $c$ is also in $C$ which is used to describe the new concept. This is also called cyclic [[Terminology|TBox]].
