---
uni-module: AI
aliases:
  - VIA
  - VI
  - Value Iteration
tags:
  - Algorithmus
---
# Value Iteration Algorithm

An [[Algorithmus|Algorithm]] to find a utility function for a [[Markov Decision Process|MDP]]. It works similar to the [[Newton Verfahren|Newton Method]] by locally approximating the utility function via the [[Bellman Equation]].

![[CleanShot 2023-09-29 at 09.59.32@2x.png]]

After finding the utility function one can retrieve the [[Optimal Policy]] by maximizing the [[Expected Utility]] over all possible [[Action|Actions]]
$$\pi[s]:=\underset{a}{\operatorname{argmax}}\left(\sum_{s^{\prime}} U\left[s^{\prime}\right] \cdot P\left(s^{\prime} \mid s, a\right)\right)$$
**Intuition**
The algorithm keeps a table $U(s)$ that is initialized with random values (e.g. $0$ or the rewards). Then in each iteration it uses the [[Bellman Equation]] to update the utility of all states. Doing this multiple times will let it slowly converge to the [[Expected Utility]] for each state. 

Delta is the maximum change in utility of any state in an iteration. If the change is below the epsilon threshold (scaled by the discount factor to accomodate for the discounting) the algorithm will terminate and return the approximate utility function. 

**Remark**
The algorithm may take long before converging to the correct utiltiy values. However the [[Optimal Policy]] can be reached quite early as the order of utilitites is found quite quickly.

Also see [[Policy Iteration Algorithm]].