# AI as Rational Agents 

- [[Rational Behavior|Rationality]]
- [[Rational Agent]]
- [[Autonomy]]
- [[Percept]]
- [[Action]]
- [[Agent Function]], [[Agent Program]], [[Agent Architecture]]
- for example [[Table-Driven Agent]]


- [[PEAS]]
- [[Performance Measure]]


There are several different types of [[Environment|Environments]]:
- [[Fully Observable Environment]]
- [[Partially Observable Environment]]
- [[Deterministic Environment]]
- [[Stochastic Environment]]
- [[Episodic Environment]]
- [[Sequential Environment]]
- [[Dynamic Environment]]
- [[Static Environment]]
- [[Semidynamic Environment]]
- [[Discrete Environment]]
- [[Continuous Environment]]
- [[Single Agent Environment]]
- [[Multi Agent Environment]]

The type of [[Rational Agent|Agent]] depends a lot on the type of [[Environment]] it is going to act in. To build an agent we need to fix an [[Agent Architecture]] and come up with an [[Agent Program]] that runs on it. There are various architectures we can choose from:

- [[Simple Reflex Agent]]
- [[Model-based Reflex Agent]]
- [[Goal-based Agent]]
- [[Utility-based Agent]]
- [[Learning Agent]]

These types of architectures can all be turned into learning agents. We also differentiate between Domain-Specific Agents and General Agents.

Representing the Environment in Agents.
Depending on the way the [[Environment]] (state) is implemented in an [[Rational Agent|Agent]] it might behave differently.
There are three different types of representation:

- atomic
- factored
	- attributes with values
- structured
	- objects with relationships

![[Bildschirm­foto 2022-12-07 um 19.00.52.png]]


## Problem Solving

An [[Rational Agent|Agent]] continuously solves the question of what [[Action]] to do next based on a state ([[Environment]]). The idea is to find actions which bring us from an **initial state** to a **goal state**. Such a sequence of actions is called a solution.

When solving problems we differentiate between [[Offline Problem Solving]] and [[Online Problem Solving]].

A problem formulation describes the problem at an abstract level. One such formulation is the math of a [[Search Problem]].

### Adversarial Search for Game Playing

- Minimax Search
- Alpha-Beta Search
- Monte-Carlo Tree Search (MCTS)


[[Constraint Satisfaction Problem]]


We want to solve problems where an [[Rational Agent|Agent]] performs certain [[Action|Actions]] in an [[Environment]]. At any given point in time we can use logical conclusions to choose a better next step by looking at the current [[Percept|percepts]] and doing _[[Inference]] / Reasoning_ ([[Automated Reasoning]]) on them.
In other words, we want the agent to think before it acts ([[Model-based Reflex Agent]]).

One way to implement such an agent would be to have a [[Knowledge Base Agent]].

Now to create this type of agent we have to be able to reason about knowledge, using [[Logic]].
One type of logic is the so called [[Propositional Logic]] where we try to describe the world by formulas which can then be evaluated in the current wolrd (they should of course turn out true).

> _[[Deduction]] is a computer trying to reason about [[Entailment|entailments]]._

In the end we want to be able to use an off-the-shelf reasoning tool (for example SAT solvers) to determine the agents best next steps.


But [[Propositional Logic]] is kind of bad for talking about real world things and it is for example impossible to speak about infinite sets of objects in it. Thus we need a new/better logic to deal with these problems, the [[First-Order Predicate Logic]].

Applications:
- Logic Programming
- Deductive [[Datenbank|Databases]]
- Semantic Technology
	- annotate [[Dataset|Data Sets]] using PL1
	- Web Ontology Language

