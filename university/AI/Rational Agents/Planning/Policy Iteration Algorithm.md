---
uni-module: AI
aliases:
  - PI
  - Policy Iteration
tags:
  - Algorithmus
---
# Policy Iteration Algorithm

This calculates a policy for a [[Markov Decision Process|MDP]].

![[CleanShot 2023-09-29 at 10.10.57@2x.png]]

**Intuition**
The algorithm starts with a random policy. The policy is then being evaluated on the current utilities (zero). 
Now for each state the algorithm tests whether there exists an [[Action]] with a bigger [[Expected Utility]] than the [[Expected Utility]] for the action from the current policy. If it finds one the policy is being updated with that better action. 
The [[Optimal Policy]] has been found, when one loop over all actions occured where no part of the policy was updated. 

The great thing is that there are way less policies than utilities. So this should in theory be better than the [[Value Iteration Algorithm]].

## Evaluation of the policy 

A fixed policy $\pi$ can be evaluated to a utility value with
$$U(s)=R(s)+\gamma\left(\sum_{s^{\prime}} U\left(s^{\prime}\right) \cdot P\left(s^{\prime} \mid s, \pi(s)\right)\right)$$