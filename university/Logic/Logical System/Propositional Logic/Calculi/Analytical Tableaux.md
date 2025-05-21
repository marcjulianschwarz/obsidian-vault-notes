---
uni-module: "AI"

alias: "Propositional Tableau Calculus"
---

# Analytical Tableaux

A [[Inference Rule|Calculus]] $\mathcal{T}_0$ with two [[Inference Rule|Inference Rules]] per connective:

![[Bildschirm­foto 2022-12-19 um 10.02.20.png]]![[Bildschirm­foto 2022-12-19 um 10.02.30.png]]

## Theorem / Derivability

$A$ is a $\mathcal{T}_0$ theorem iff there is a closed tableau with $A^F$ at the root (this also shows that $A$ is valid).
A set of formulas $\Phi$ (assumptions) can be used to derive $A$ iff there is a closed tableau starting with $A^F$ and this set of assumptions.
If we have the second case with only one branch, then this is called initial for $\Phi \vdash_{\mathcal{T}_0} \mathrm{~A} .$


