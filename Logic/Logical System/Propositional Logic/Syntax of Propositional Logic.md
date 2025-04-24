---
uni-module: "AI"
---

# Syntax of Propositional Logic

Formulas of $PL^0$ are made up from:

- countably infinite propositional variables
  - $\mathcal{V}_0:=\left\{P, Q, R, P^1, P^2, \ldots\right\}$
- connectives
  - $\Sigma_0:=\{T, F, \neg, \vee, \wedge, \Rightarrow, \Leftrightarrow, \ldots\}$
- well-formed propositional formulas (wffs)
  - propositional variables
  - $T$ true and $F$ false
  - negations
  - [[Konjunktion|Conjunction]]
  - [[Disjunktion]]
  - [[Implikation|Implication]]
  - equivalences / biimplications
  - where the variables used for the formulas are again wffs

A single formula without any connectives is called an [[Atom]].

The list above can be formulated in terms of a [[Backus-Naur-Form|Grammar]]:

![[Bildschirm­foto 2022-12-19 um 09.10.42.png]]

