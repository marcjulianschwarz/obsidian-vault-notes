---
uni-module: AI
aliases:
  - MDP
---
# Markov Decision Process

A MDP is used in a [[Fully Observable Environment|fully observable]] but [[Stochastic Environment]]. This means all states are known but the [[Action|Actions]] of an [[Rational Agent|Agent]] are not deterministic. 

It consists of 
- a set of states $S$
- an initial state $s_0\in S$
- sets of actions for each state $\operatorname{Actions}(s)$
- [[Übergangsmatrix|Transition Model]] $P(s'\mid s, a)$
- a reward function $R: S \rightarrow \mathbb{R}$
	- with reward $R(s)$

We only look at Markovian transition models and additive reward functions.

The [[Optimal Policy]] depends on the reward for each state. There is always a risk and reward tradeoff. 

![[CleanShot 2023-09-29 at 09.31.51@2x.png]]

## Fully Observable MDPs

Now to work with a [[Markov Decision Process]] we need utility over time which we introduce via [[Preferences on Reward Sequences]]. The additive way of combining rewards to a utility function becomes a problem when we consider the infinite lifetime of an [[Rational Agent|Agent]]. The utility becomes infinite.

To fix this we could 
- terminate utility computation at fixed time 
- introduce absorbing states which for any policy will end the agents life 
- use discounting factor to dampen the reward when going towards infinity 

For all of the ideas we want for an [[Optimal Policy]] that we have constant average reward per time step after some time. 
Currently we still only have utility for a set of states but we want utility for one state. To do this we use 
$$U^\pi(s):=E\left[\sum_{t=0}^{\infty} \gamma^t R\left(s_t\right)\right]$$
This is the [[Expected Utility]] we get by executing the policy $\pi$ starting from state $s$ until the agent terminates.
We can now define the [[Optimal Policy]] as the policy with the maximum [[Expected Utility]] in the current state.
$$\pi_{\boldsymbol{s}}^*:=\underset{\pi}{\operatorname{argmax}} U^\pi(\boldsymbol{s}) .$$
It is important to note that this [[Optimal Policy]] is independent of the current state so we can even say that it is optimal for all states. This however does not hold for finite horizon policies.

We could say $R(s)$ is the short term reward when doing one [[Action]] and $U(s)$ is the long term reward as it contains a sequence of actions that might lead to a higher reward than only the next action. 

We can observe a simple relationship between neighboring states which gives us the [[Bellman Equation]]. This equation is recursive so we can use an iteration algorithm to approximate the utility function with it. This is done in the [[Value Iteration Algorithm]].

The [[Policy Iteration Algorithm]] goes a different route and approximates the [[Optimal Policy]] instead.

A combination of [[Value Iteration Algorithm|VI]] and [[Policy Iteration Algorithm|PI]] often converges a lot faster.

## Partially Observable MDPs 

[[Partially Observable MDP]]
