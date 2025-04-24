---
uni-module: AI
aliases:
  - Preference
---
# Preferences

Given states (prizes) $A$ and $B$, an [[Rational Agent|Agent]] can express preferences of the form 

For [[Deterministic Environment|deterministic environments]] we know all possible states so we can always state preferences in the following way.

$A$ is preffered over $B$
$$A \succ B$$
$A$ and $B$ are the same
$$A \sim B$$
$B$ is **not** preferred over $A$ but it would not matter when $A$ is preffered 
$$A\succeq B$$

In a [[Stochastic Environment]] however we do not have full information about the states. So we use the states [[Prior Probability|Priors]] in a **lottery**.
$$\left[p_1, A_1 ; \ldots ; p_n, A_n\right].$$

A set of preferences is called [[Rational Behavior|rational]] iff the following constraints hold: 

> [!purple-highlight]+ Orderability
> $A \succ B \vee B \succ A \vee A \sim B$

> [!purple-highlight]+ Transitivity
> $A \succ B \wedge B \succ C \Rightarrow A \succ C$
> also see [[Transitivität|Transitivity]]

> [!purple-highlight]+ Continuity
> $\boldsymbol{A} \succ B \succ C \Rightarrow(\exists \boldsymbol{p} \cdot[\boldsymbol{p}, \boldsymbol{A} ; \mathbf{1}-\boldsymbol{p}, C] \sim B)$

> [!purple-highlight]+ Substitutability
> $A \sim B \Rightarrow[p, A ; 1-p, C] \sim[p, B ; 1-p, C]$

> [!purple-highlight]+ Monotonicity
> $A \succ B \Rightarrow(p>q) \Leftrightarrow[p, A ; 1-p, B] \succ [q, A ; 1-q, B]$

> [!purple-highlight]+ Decomposability
> Lotteries in a lottery can be decomposed into a big lottery via their probabilities.
> 
> $[p, A ; 1-p,[q, B ; 1-q, C]] \sim[p, A ;((1-p) q), B ;((1-p)(1-q)), C]$

For all constraints we could construct an example where an agent would act irrational if the constraint would not hold. 

Also see [[Preferences on Reward Sequences]] for [[Markov Decision Process|MDP]].