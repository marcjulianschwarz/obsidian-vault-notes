# Logic-Based Planning

We can represent the Wumpus rules in a [[Logical System]] (e.g. [[Propositional Logic]], [[First-Order Predicate Logic]], [[ALC]]) and use [[Inference]] to deduce new knowledge from [[Percept|percepts]] and [[Action|actions]]. This representation will result in contradictions when the agent moves through the world and its percepts are changing.

The obvious idea is to make the representations of percepts time-dependent.
[[Fluent]], [[Atemporal]].

- [[Model-based Reflex Agent]]
- [[Knowledge Base Agent]]

We want an [[Rational Agent|Agent]] that can deal with time. For example we would like to be able to express something like this:
$$\forall t, x, y . \operatorname{Ag} @(t, x, y) \Rightarrow \operatorname{draft}(t) \Leftrightarrow \operatorname{breeze}(x, y) .$$
But how do we get a [[Fluent]] like: the agent is at $x,y$ at time $t$ ? Has to do with [[Transition Model]] where we get the state of the [[Environment]] after an [[Action]] (so for example new cell position).

We can use [[Fluent|fluents]] to describe actions in so called **Effect Axioms**.
For example:
![[Bildschirm­foto 2023-02-02 um 16.40.34.png]]

[[Frame Problem]]

Hybrid Agent → special code for Wumpus world example.

However, we want: General Planning Agent.
