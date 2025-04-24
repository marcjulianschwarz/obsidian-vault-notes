---
uni-module: "AI"

alias: ["TBox", "Isa Hierarchy"]
---

# Terminology

This is the [[Teilgraph|Subgraph]] of a [[Semantic Network]] spanned by the isa links and relations between [[Concept|concepts]].

Usually you want to have a small [[Terminology|TBox]] that is really precise. Because [[Inference]] is done on the [[Terminology|TBox]] and not on the [[Assertion|ABox]]. The [[Assertion|ABox]] may contain a LOT of objects.

A [[Terminology|TBox]] is called **acyclic** when it does not contain recursive [[Concept Definition|concept definitions]].

A formula is called **normalized** with respect to a TBox iff it does not contain [[Concept|concepts]] defined in $\mathcal{T}$. So we can use [[Concept Definition|concept definitions]] to normalize a formula back to its original properties by substituting $c$ by $C$.
For acyclic TBoxes this normalization will termintate but results can get [[Exponential Growth|exponentially]] large.

![[Bildschirm­foto 2023-01-31 um 16.42.36.png]]
