---
uni-module: AI
---
# Preferences on Reward Sequences 

For an [[Markov Decision Process|MDP]] we want to focus on [[Preferences]] on reward sequences to get a sense of time. 

We call such preferences **stationary** iff 
$$\left[r, r_0, r_1, r_2, \ldots\right] \succ\left[r, r_0^{\prime}, r_1^{\prime}, r_2^{\prime}, \ldots\right] \Leftrightarrow\left[r_0, r_1, r_2, \ldots\right] \succ\left[r_0^{\prime}, r_1^{\prime}, r_2^{\prime}, \ldots\right]$$
This means, if we remove the first reward from the sequences we still have the same preference. 

For these types of preferences there are two ways to combine them over time to get a utility function for a sequence of states.

**Additive**
$$U\left(\left[s_0, s_1, s_2, \ldots\right]\right)=R\left(s_0\right)+R\left(s_1\right)+R\left(s_2\right)+\cdots$$
**Discounted**
$$U\left(\left[s_0, s_1, s_2, \ldots\right]\right)=R\left(s_0\right)+\gamma R\left(s_1\right)+\gamma^2 R\left(s_2\right)+\cdots$$
with discount factor $\gamma.$