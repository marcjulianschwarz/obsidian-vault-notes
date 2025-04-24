---
uni-module: "AI"

alias: "Logic"
---
# Logical System

A logical system is a triple $\mathcal{S}:=\langle\mathcal{L}, \mathcal{K}, \models\rangle$ where

- $\mathcal{L}$ is a formal language
- $\mathcal{K}$ is a set
- and $\models \subseteq \mathcal{K} \times \mathcal{L}$

Members of $\mathcal{L}$ are called formulas of $\mathcal{S}$.
Members of $\mathcal{K}$ are called models for $\mathcal{S}$
And $\models$ is the **satisfaction relation**.

One example of such a logical system is the [[Propositional Logic]]:
$$\left\langle w f f\left(\Sigma_0, \mathcal{V}_0\right), \mathcal{K}, \models\right\rangle$$
where we define $\mathcal{K}$ as the set of [[Variable Assignment|variable assignments]]:
$$\mathcal{K}:=\mathcal{V}_0 \rightarrow \mathcal{D}_0$$
and we say an assignment entails $A$ if its meaning [[Interpretation Function|interpretation]] is equal to true.

Now let there be a logical system with $\mathcal{M}\in \mathcal{K}$ a model and $A\in \mathcal{L}$ a formula, the we say that $A$ is:

- satisfied by $\mathcal{M}$ iff $\mathcal{M}$ entails $A$
- satisfiable if there exists a $\mathcal{M}\in \mathcal{K}$ which satisfies $A$
- unsatisfiable if there doesnt exist a $\mathcal{M}\in \mathcal{K}$ which satisfies $A$
- valid if every $\mathcal{M}$ satisfies $A$
- falsified by $\mathcal{M}$ iff $\mathcal{M}$ does not entail $A$
- falsifiable if there exists a $\mathcal{M}\in \mathcal{K}$ which falsifies $A$

[[Inference Rule|Calculus]]

[[Logical System]] + [[Derivation Relation]] = [[Formal System]]
