---
uni-module: "AI"

alias: ["PL0", "Aussagenlogik"]
---

# Propositional Logic

> Canonical Form of knowledge and reasoning on that knowledge.

How can we capture [[Deduction]]?
How can we make [[Deduction]] mechanizable?

- [[Analytical Tableaux]]
- [[Resolution Calculus|Resolution]] → underlying most successful [[Erfüllbarkeitsproblem der Aussagenlogik|SAT]] solvers

The propositional logic can be fully defined by the

- [[Syntax of Propositional Logic]]
- [[Semantics of Propositional Logic]]


> [!NOTE] Difference between Syntax and Semantics
> **Syntax**: legal formulas in a logic.
> **Semantics**: which formulas are true under which [[Variable Assignment]]? Written $\varphi \models \mathbf{A}$

We can observe that the set of well-formed formulas is a **formal language** over the alphabet given by $\mathcal{V}_0$ the variables/atoms, the connectives and brackets.
For such languages we are mostly interested in Satisfiability and [[Entailment]].


With [[Deduction]] we try to derive certain statements from a list of formulas using a set of [[Inference Rule|Inference Rules]].
Applied to the agent-world-model we try to derive actions from a current state using some set of rules (possible actions, etc...).

[[Soundness]] and [[Completeness]] are two properties of a [[Inference Rule|Calculus]].

## Propositional identities

These identities might be helpful in proofs:

![[Bildschirm­foto 2022-12-19 um 09.29.39.png]]

## Predicate Logic Without Quantifiers

Instead of talking about rather abstract objects like the propositional variables we want to replace them with something more expressive.

First Order Signature
Function Constants
Predicate Constants

Isomorphism between $PL_{NQ}$ and $PL^0$

## Inference

As stated earlier we need to have some rules on which we base our [[Deduction]]. A set of these [[Inference Rule|Inference Rules]] is also called a [[Inference Rule|Calculus]] of which there can be many.

One such simple system is the [[Hilbert Calculus]]. In this system we can proof/derive formulas. The fact that formal derivations are actually true in the real world makes this tool extremly useful.

### Natural Deduction Calculus

The [[Natural Deduction]] [[Inference Rule|Calculus]] $\mathcal{ND}_0$ tries to mimic human argumentation for theorem proving (basic methods for proof are being used here as [[Inference Rule|Inference Rules]]).

Now in [[Sequent Calculus Formulation]] we represent hypothesis explicitly. We can use this type of formulation to get a [[Linearized Notation for sequent-style ND proofs]].

### Machine-Oriented Calculi

We would like to automate theorem proving by making our logic more usable by computers.

A **[[Formal System]]** consists of

- conjectures $C\in \mathcal{L}$
- hypotheses $\mathcal{H}\subseteq \mathcal{L}$

Now the task of proving a theorem is to determine whether we have $\mathcal{H} \vdash C$.

The task of **automated** theorem proving (ATP) consists of developing a [[Inference Rule|Calculus]] for the [[Logical System]] and being able to create programs that can test whether a given set of hypothesis entail a conjecture. This is usually done by searching for derivations $\mathcal{H} \vdash_{\mathcal{C}} \mathrm{A}$ in that [[Inference Rule|Calculus]].

So the main idea is, that ATP now induces a [[Search Problem]] where the states are sets of formulas, the [[Action|actions]] are [[Inference Rule|Inference Rules]] from the Calculus and the initial state are the assumptions. The goal states are those wich include the to be proven theorem.

However it is hard to find good heuristics for this search problem and we thus want to use the [[Unsatisfiability Theorem]] instead.

So we don't try to derive $A$ but instead derive the falsified version of $A$ and end in an unsatisfiable formula. This is called a **Test Calculus**.

So we now have a different [[Search Problem]] where the initial state are the assumptions together with the falsified theorem and the goal state is reached when there is a closing symbol.

### Normal Forms

An [[Atom|atomic]] [[Labeled Formula]] is called [[Positive Literal]] when its label is true and [[Negative Literal]] when its label is false. Also see [[Opposite Literal]].

The intuition behind the next chapter ([[Analytical Tableaux]]) is that we think of satisfying a formula as making it have the truth value of its label $\alpha$.

Also note that there is also the alternative definition of literals without the labeling part which is equivalent but doesnt generalise that well for logics with more than two truth values.

Every formula can be rewritten to an equivalent formula in the form of

- [[Conjunctive Normal Form]]
- [[Disjunctive Normal Form]]


### Analytical Tableaux, Practical Enhancements for Tableaux, Soundness and Termination of Tableaux

Now the idea is to develop a so called Test [[Inference Rule|Calculus]] that

- analyzes a [[Labeled Formula]] [[Baum|Tree]] to determine satisfiability
- its branches correspond to models (valuations)

This is called the [[Analytical Tableaux]]

### Resolution for Propositional Logic

We now want to introduce another Test Calculus, the [[Resolution Calculus]].

- [[Clause]]
- [[Empty Clause]]
- [[Unit Clause]]

[[CNF Transformation Calculus]]

Clause Set Simplification

## SAT 

The [[Erfüllbarkeitsproblem der Aussagenlogik|SAT]] problem is, given a formula decide whether or not it is satisfiable. It was the first problem to be proven to be [[Nondeterministic Polynomial Time Complete|NPC]].

The Davis-Putnam (Logemann-Loveland) Procedure
- [[Davis Putnam Procedure]]
- [[Unit Propagation]]

- DPLL Restriced Form of Resolution
- Why did Unit Propagation yield a Conflict?
- Clause Learning