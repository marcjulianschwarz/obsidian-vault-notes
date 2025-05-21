---
uni-module: "AI"
---
# Partial Order Planning

The process of computing [[vollständig|complete]] and acyclic [[Partially Ordered Plan]] for a given [[Planning Task]].

Some subgoals need to be done in sequence and others dont.

Any [[Algorithmus|algorithm]] that can place two [[Action|actions]] into a [[Plan]] without specifying which comes first.

Idea:

- use [[Directed Acyclic Graph|DAG]] that supports multiple paths from initial states to goal states
  - nodes = actions
  - edges = [[Precondition]], Add List, Delete List ([[Effect]])

Acyclic → partial ordering

## Advanatges:

- problems can be decomposed
- efficient by least-commitment strategy
- causal links will pinpoint unworkaple plans early

[[Clobbering]] conflicts can be resolved by:

- [[Promotion]]
- or [[Demotion]]

We are doing problem description level search and not state space level search. This is some form of thightening.

[[POP Algorithm]]
