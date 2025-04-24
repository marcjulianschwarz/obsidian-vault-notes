---
uni-module: "AI"

alias: "Unifikation"
---

# Unification

For given [[Terms]] $A$ and $B$, unification is the problem of finding a substitution $\sigma$ such that:
$$\sigma(A)=\sigma(B)$$
This means we want to make them **syntactically** equal. We dont do equation solving in the usual way here.

We can ask for such a unification with the following notation:
$$A=^?B$$
Solutions to this problem are called **unifiers**.

So we want to find representatives in
$$U((A=^?B))=\{\sigma|\sigma(A)=\sigma(B)\}$$
that generate the set of solutions.

Looking at some simple examples one can quickly see that there are lots of solutions for this problem, which is bad. We want to have the minimal commitment solution. Because when doing the [[Free Variable Tableau Calculus]] Tableau, we might end up closing lots of things in it when instantiating the whole tableau with our substitution.

[[Constraint Satisfaction Problem|CSP]] is a generalisation of Unification (compare with tightness).
