---
uni-module: "AI"

alias: ["PL1", "Prädikatenlogik erster Stufe", "FOL"]
---

# First-Order Predicate Logic

A [[Formal System]] used in a lot of fields of science. It combines [[Propositional Logic]] with the ability to quantify over individuals.

PL1 talks about two kinds of objects:

- truth values (the same as in [[Propositional Logic|PL0]])
- individuals

[[First-Order Signature]]

We talk about [[Terms]], [[Proposition|Propositions]], [[Universal Quantifier]], [[Existential Quantifier]] and other connectives.

- [[Bound Variable]]
- [[Free Variable]]

[[Closed Formula]]
[[Sentence]]

- The set of all [[Closed Formula|ground]] [[Terms]] → $\text{cwff}_l(\Sigma_l)$
- The set of [[Sentence|sentences]] → $\text{cwff}_o(\Sigma_o)$

Any [[Bound Variable]] can be renamed, which means that any subterm

[[Alphabetical Variant]]

## Evaluation of First Order Predicate Logic

We inherit the [[Universe]] of truth values from the [[Propositional Logic]] and assume another universe $\mathcal{D}_l\neq \emptyset$ of individuals.

We again have an [[Interpretation Function]] which we use from [[Propositional Logic|PL0]] and add interpretations for

- functions → arbitrary functions $\mathcal{D}^k\rightarrow \mathcal{D}_l$
- predicates → arbitrary relations $\mathcal{P}((\mathcal{D}_l^k))$

We also use a [[Variable Assignment]] to map variables into the universe, here into the universe of individuals from the variables (individuals).

A model of PL1 consists of

- a universe
- an [[Interpretation Function]]

Evaluation of the [[Interpretation Function]]:

![[Bildschirm­foto 2023-01-30 um 16.58.55.png]]
[[Assignment Extension]]

Semantics Computation Example:
![[Bildschirm­foto 2023-01-31 um 09.14.46.png]]

It can talk about:

- individual things
- properties of these things
- relations between these things
- functions on these things
- the existence of a thing with a certain property
- the universality of a property

This logic has many good properties:

- [[Kompaktheit|compactness]]
- unitary
- linear unification

But it is too weak for formalizing:

- natural numbers, [[Inference Rule|Calculus]], etc.
- [[Generalized Quantifiers]]

## First-Order Natural Deduction 

- [[First-Order Natural Deduction]]
- [[First-Order Natural Deduction in Sequent Formulation]]
- [[First-Order Natural Deduction with Equality]]
- [[First-Order Predicate Logic with Equality]]

## Automated Theorem Proving in First-Order Logic

- [[Standard Tableau Calculus]]
- [[Free Variable Tableau Calculus]]

## First-Order Unification 


[[Unification]]
[[More General]]
[[Most General Unifier]]

### Naive calculation:

Idea: get a [[Unification]] algorithm from a [[Inference Rule|Calculus]], so basically write down the rules and let it run.

[[Solved Form]]
[[Unification Algorithm]]

### Efficient Unification

Consider the example [[Unification Problem]] of:

$$
\begin{aligned}
& s_n=f\left(f\left(x_0, x_0\right), f\left(f\left(x_1, x_1\right), f\left(\ldots, f\left(x_{n-1}, x_{n-1}\right)\right) \ldots\right)\right) \\
& t_n=f\left(x_1, f\left(x_2, f\left(x_3, f\left(\cdots, x_n\right) \cdots\right)\right)\right.
\end{aligned}
$$

Even printing the solution ([[Most General Unifier|MGU]]) for this problem is exponential. It contains $2^{n+1} - 2$ occurrences of the variable $x_0$.

However there are algorithms that can decide whether the problem is unifiable or not in linear time.

An idea to solve this exponential nature of the algorithm is to find a term representation that re-uses subterms. We recall that [[First-Order Predicate Logic]] [[Terms]] can be represented using trees, which would get exponentially big in the example from above.
Terms can be transformed into [[Directed Acyclic Graph|DAG]]s in linear time. So we can see that we only need linear space $\mathcal{O}(n)$ in that case.

![[Bildschirm­foto 2023-01-31 um 14.31.42.png]]
