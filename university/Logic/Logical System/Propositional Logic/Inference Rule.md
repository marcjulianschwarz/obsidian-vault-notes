---
uni-module: "AI"

alias: ["Inference Rules", "Calculus", "Inference System"]
---

# Inference Rule

A set of inference rules is called a calculus or inference system for a [[Logical System]].

A logical system can have a formal language $\mathcal{L}$, then [[Inference Rule|Inference Rules]] over that language are a decidable $n+1$ relation. Such rules can be written as:
![[Bildschirm­foto 2023-01-29 um 14.19.18.png]]
where the $A_i$ are called assumptions and $C$ is called its conclusion.

No assumptions → [[Axiom]].

An inference rule is called **admissible** in a calculus if the extension of the calculus by that rule does not yield any new theorems.
This means all derivable inference rules are admissible as we can always use the rules that were used for the derivation. This does not hold the other way around.

## Examples of Calculi

- [[Hilbert Calculus]]
- [[Natural Deduction]]
- [[Analytical Tableaux]]
- [[Resolution Calculus]]
- [[CNF Transformation Calculus]]

