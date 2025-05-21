---
uni-module: "AI"

alias: "DPLL"
---

# Davis Putnam Procedure

A [[Erfüllbarkeitsproblem der Aussagenlogik|SAT]] solver called on a [[Clause]] set with the empty assignment. It uses [[Unit Propagation]] and Splitting.

## Explanation

### Inputs

- Clause Set $\d$
- Accumulator for the partial assignment $I$

### Unit Propagation

While there are still [[Unit Clause|unit clauses]] left in the clause set:

- extend the partial assignment with the truth value of the current clause
- when the clause set is an empty set return the message unsatisfiable
- when there are no more clauses in the set return the current assignment

### Splitting Rule

Select any proposition which is not defined in the current partial assignment.
Now recursively call the procedure on:

1. The assignment extended by one truth value for the selected proposition
2. The assignment extended by the other truth value for the selected proposition

Return assignment when one of the splits is not unsatisfiable, else recurse further.

![[Bildschirm­foto 2023-01-29 um 21.39.03.png]]

## Examples

![[Bildschirm­foto 2023-01-29 um 21.46.49.png]]
![[Bildschirm­foto 2023-01-29 um 21.46.58.png]]
