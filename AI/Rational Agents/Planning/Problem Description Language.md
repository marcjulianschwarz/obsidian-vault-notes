---
uni-module: "AI"

alias: "Planning Language"
---

# Problem Description Language

A Problem Description Language is a logical language for the components of a [[Search Problem]].
So basically a level higher than the previous logics [[Propositional Logic]] and [[First-Order Predicate Logic]].

In particular it describes:

- possible states (predicates)
- initial state $I$
- goal test $G$
- set $A$ of [[Action|actions]] in terms of
  - [[Precondition]]
  - [[Effect]] (replaces Frame Axioms in [[Frame Problem]])
  - (compare with [[Transition Model]])

A logicial description of all of these parts is called a [[Planning Task]]. And a solution to this is called [[Plan]] which we try to find via planning.
