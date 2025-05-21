---
uni-module: AI
aliases:
  - POMDP
---
# Partially Observable MDP

A [[Markov Decision Process]] together with a [[Sensor Model]] $O$ that has the [[Sensor Markov Property]] and is stationary, which means 
$$O(s,e)=P(e\mid s).$$
This models a [[Partially Observable Environment|partially observable]] and [[Stochastic Environment|stochastic]] environment. As the [[Rational Agent|Agent]] does not know which state it is in, it makes no sense to talk about policies that map concrete states to [[Action|Actions]]. 
Thus we introduce the [[Optimal Policy]] as a function 
$$\pi^*(b)$$
that maps [[Belief State|belief states]] to actions instead.

Now the idea is to convert a POMDP into an [[Markov Decision Process|MDP]] in [[Belief State]] space. Which means we want to have a [[Übergangsmatrix|Transition Model]] on the belief states and a reward function on the belief states.

## Filtering at the Belief State Level 

$$b^{\prime}\left(s^{\prime}\right)=\operatorname{FORWARD}(b,a,e)=\alpha \cdot P\left(e \mid s^{\prime}\right) \cdot\left(\sum_s P\left(s^{\prime} \mid s, a\right) \cdot b(s)\right)$$

> [!orange-highlight]- Overview Formula
> ![[IMG_C57EF646A1A7-1.jpeg]]
> [[Übergangsmatrix|Transition Model]]
> [[Sensor Model]]
> [[Belief State]]

**POMDP Decision Cycle**
- Given current [[Belief State]] $b$, execute [[Action]] $a=\pi^*(b)$
- Receive [[Percept]] $e$
- Update [[Belief State]] with $\operatorname { FORWARD }(b, a, e)$

## Reducing POMDPs to Belief State MDPs 

[[Übergangsmatrix|Transition Model]] at the [[Belief State]] level 

$$\begin{aligned}
P\left(b^{\prime} \mid b, a\right) & =P\left(b^{\prime} \mid a, b\right)=\sum_e P\left(b^{\prime} \mid e, a, b\right) \cdot P(e \mid a, b) \\
& =\sum_e P\left(b^{\prime} \mid e, a, b\right) \cdot\left(\sum_{s^{\prime}} P\left(e \mid s^{\prime}\right) \cdot\left(\sum_s P\left(s^{\prime} \mid s, a\right), b(s)\right)\right)
\end{aligned}$$

where $P\left(b^{\prime} \mid e, a, b\right)$ is $1$ if $b^{\prime}=\operatorname{FORWARD}(b, a, e)$ and 0 otherwise. 

Reward function at the [[Belief State]] level. 
$$\rho(b):=\sum_s b(s) \cdot R(s)$$
The expected reward for the states the [[Rational Agent|Agent]] might be in.

Now we reduced the POMDP to a [[Markov Decision Process]] with a [[Übergangsmatrix|Transition Model]]
$$P\left(b^{\prime} \mid b, a\right)$$
and a reward function 
$$\rho(b).$$
This is actually observable now as the [[Belief State]] state is **always** observable. 

An [[Optimal Policy]] on this MDP is also an optimal policy on the POMDP. 