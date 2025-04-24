---
uni-module: "AI"
---

# Search Problem

A search problem can be a 
- [[Single State Problem]],
- [[Multi State Problem]]
- [[Contingency Problem]]

A search problem has the form $\Pi:=\langle\mathcal{S}, \mathcal{A}, \mathcal{T}, \mathcal{I}, \mathcal{G}\rangle$ and it consists of:
- A set of states $\mathcal{S}$
- A set of [[Action|actions]] $\mathcal{A}$
- A [[Transition Model]] $\mathcal{T}$
- Certain **goal states** $\mathcal{G}\subseteq \mathcal{S}$
- Certain **initial states** $\mathcal{I}\subseteq \mathcal{S}$

An action is called **applicable** in a state if the [[Transition Model]] is not the empty set with that action and state. We can constrain the [[Transition Model]] to a certain action and get the **result relation** for that action. By constraining the model to the whole set of actions in the search problem we get the result relation of the whole search problem.

The **state space** induced by the search problem is the [[Graph]] $\left\langle\mathcal{S}, \mathcal{T}_{\mathcal{A}}\right\rangle$.

## Solution

A solution is a sequence of actions such that all actions are **applicable** to the state before taking the action where the state at time zero is in the set of **initial states**. The current state **must be in the set of successor states** determined by the transition model on the current action and the previous state. The last state must be part of the set of **goal states**.

Additionally we can add a cost function that assigns a step cost to an action. Then the costs of a solution is the sum over the step costs of all actions in that solution.

When selecting a state space one has to know how much the space should be asbstracted. Too much detail can make the space too big.

### Idea of solving a search problem

We know that the state space of a problem is a [[Graph]]. However graphs are difficult to compute with. We thus create a corresponding [[Baum|Tree]] and work on that.

The **Tree Search Algorithm** consist of the simulated exploration of the state space by successively expanding already-explored states (It is thus an offline algorithm).

Could look like this in pseudo code:

```
initialize tree with initial state
loop
	if no candidates for expansion:
		return failure
	choose leaf node for expansion according to strategy
	if node contains goal state:
		return solution
	else:
		expand node and add nodes to search tree
```

![[Bildschirm­foto 2022-11-26 um 12.37.46.png]]

[[Fringe]]
Strategy

### Uninformed Tree Search Algorithms:

An uninformed search algorithm only used the available information of the problem definition.
Examples are:
- [[Breadth-first search]]
- Uniform-cost search (UCS)
- [[Depth-first search]]
- [[Depth-limited search]]
- [[Iterative Deepening search]]

### Informed Tree Search Algorithms:
