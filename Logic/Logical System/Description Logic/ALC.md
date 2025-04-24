---
uni-module: "AI"
---

# ALC

[[Propositional Logic]] is not [[Expressive Adequacy|expressive]] enough as there are no quantifiers. So we try to use [[First-Order Predicate Logic]]. This however is too expressive and this algorithms are too complex and don't terminate.
So the idea is to have a logic that is more expressive than [[Propositional Logic]] but weaker than [[First-Order Predicate Logic]].

[[Concept]]
[[Role]]

## Syntax

Grammar for ALC:

![[Bildschirm­foto 2023-02-01 um 10.30.42.png]]

[[Concept Definition]] work here too.
We can also do Normalization of [[Concept Definition]], which can get exponential for cyclic/recursive definitions.

## Semantics

[[Interpretation Function]] $[[\circ]]$

![[Bildschirm­foto 2023-02-01 um 10.34.47.png]]

or alternitavely via [[Translation into First-Order Predicate Logic]] by extending the translation with these rules:

![[Bildschirm­foto 2023-02-01 um 10.35.35.png]]
These rules more or less guard away formulae which would make ALC undecidable.

Some Identities:

![[Bildschirm­foto 2023-02-01 um 10.39.49.png]]

Use these identities to formulate the [[Negation Normal Form]]

![[Bildschirm­foto 2023-02-01 um 10.40.55.png]]
We define [[Assertion|assertions]] for ALC:

- $a:\varphi$ → $a$ is a $\varphi$
- $\text{a R b}$ → $a$ stands in relation $R$ to $b$

These make up the [[Assertion|ABox]] in ALC.

Their semantics are:
![[Bildschirm­foto 2023-02-01 um 10.45.34.png]]

We also extend the translation into first order logic:

![[Bildschirm­foto 2023-02-01 um 10.46.01.png]]
## Inference 

[[ALC Tableau Calculus]]
