---
uni-module: "AI"
---

# Propositional Logic as Set Description Language

Used for the [[Semantic Web]].

Let $PL_{DL}^0$ be given by the following grammar for concepts:

$$\mathcal{L}::=C|\top| \perp|\overline{\mathcal{L}}| \mathcal{L} \sqcap \mathcal{L}|\mathcal{L} \sqcup \mathcal{L}| \mathcal{L} \sqsubseteq \mathcal{L} \mid \mathcal{L} \equiv \mathcal{L}$$
So we have:

- atomics
- [[Concept]] intersection (and)
- concept complement (negation)
- concept union (or)
- concept subsumption ([[Implikation|implication]])
- concept equality (equivalence)

We can use all of our propositional identities that we already proved for [[Propositional Logic]]:

![[Bildschirm­foto 2023-01-31 um 17.17.11.png]]

So we can actually compute with these.

And we are able to translate back to [[Propositional Logic]] and then over to [[First-Order Predicate Logic]]:

→ [[Translation into First-Order Predicate Logic]]

### Examples for this

![[Bildschirm­foto 2023-01-31 um 17.20.50.png]]
