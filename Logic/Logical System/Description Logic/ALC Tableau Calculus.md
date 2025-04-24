---
uni-module: "AI"
---

# ALC Tableau Calculus

The [[ALC]] Tableau [[Inference Rule|Calculus]] acts on [[Assertion|assertions]]:

- $x:\varphi$
- $\text{x R y}$

where $\varphi$ is a normalized [[Concept]] in [[Negation Normal Form|NNF]].

We have the following [[Inference Rule|Inference Rules]]:

![[Bildschirm­foto 2023-02-01 um 10.48.46.png]]

In the fourth rule you can see that the [[Universal Quantifier]] is guarded by the relation. This is the part where the [[Standard Tableau Calculus]] was failing because there we would have to test all possible assertions and not only the ones in the relation.

The last rule basically introduces another witness (Skolem... ).

This calculus is

- [[Soundness|sound]]
- and [[Completeness|complete]]
