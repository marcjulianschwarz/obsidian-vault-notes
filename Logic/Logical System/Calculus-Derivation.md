---
uni-module: "AI"
---

# Calculus-Derivation

Let $\mathcal{S}$ be a [[Logical System]] system and $\mathcal{C}$ a [[Inference Rule|Calculus]] for $\mathcal{S}$, then a $\mathcal{C}$ derivation of a formula $C\in \mathcal{L}$ from a set of hypotheses $\mathcal{H}\subseteq \mathcal{L}$, also written as $\mathcal{H} \vdash_{\mathcal{C}} C$, is a sequence of $A_i$ $\mathcal{L}$ formulas, such that:

- the derivation culminates in $C$
- all $A_i$ are either part of the hypotheses or
- there is an [[Inference Rule|Inference Rule]] which derives $A_i$

We can think of a derivation as a derivation [[Baum|Tree]] where the $A_{lj}$ are children of the node $A_k$ for an inference rule that looks like this:

![[Bildschirm­foto 2023-01-29 um 14.33.45.png]]
