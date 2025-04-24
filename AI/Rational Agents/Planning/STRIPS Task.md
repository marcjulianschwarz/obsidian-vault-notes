---
uni-module: "AI"
---

# STRIPS Task

A quadruple $\Pi:=\langle P, A, I, G\rangle$ where

- $P$ is a finite set of facts (propositions)
- $A$ is a finite set of [[Action|actions]]
  - each action is a tripe of subsets of the facts
    - [[Precondition]]
    - Add List (true after action is done)
    - Delete List (false after action is done)
    - where the intersection of the add and delete list is empty
- $I\subseteq P$ is the initital state
- $G\subseteq P$ is the goal state

We can give actions a name (string) and assume that every action has a cost of 1.

We try to generate a [[Search Problem]] from a [[STRIPS]] task.

Search Problem:

- states are conjunctions of facts (so [[Potenzmenge]])
- actions are the same
- [[Transition Model]]:
  - applying action to state is only possible when actions [[Precondition]] is met → action is applicable
  - then apply-function of transition model adds the Add List to the state and deletes the Delete List from the state
- goal states is the same (goal state is in the current state)
- initial states is the same
- solutions: paths from initital state to goal state
  - for example: [[Iterative Deepening search]] on state space

Problem:
The states in the [[Search Problem]] also include parts that are not reachable in the [[Planning Task]].

[[Blocks World]]
[[Miconic-10]]
