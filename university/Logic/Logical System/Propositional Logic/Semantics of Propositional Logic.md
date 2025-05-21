---
uni-module: "AI"
---

# Semantics of Propositional Logic

The semantics are a model $\mathcal{M}$ consisting of a [[Universe]], which in this case are the two formulas $T$ and $F$, and an [[Interpretation Function]] which describes the meaning of the connectives.

$$\mathcal{M}=<\mathcal{U},\mathcal{I}>$$

Both the [[Interpretation Function]] and the [[Variable Assignment]] function are used to define the [[Value Function]] which assigns values from the [[Universe]] to formulas.

Using the above model we can compute the semantics for a given formula. This however is quite a mess... (see slides for example).
A simpler form to compute the semantics by hand would be something like a truth table.

### Semantic properties

Some important properies of formulas are:

- true under [[Variable Assignment]]
- false under [[Variable Assignment]]
- satisfiable if there exists a [[Variable Assignment]] making the formula true
- valid if the model entails the formular for all assignments
- falsifiable if there exists a [[Variable Assignment]] making the formula false
- unsatisfiable if all [[Variable Assignment|assignments]] make the formula false
