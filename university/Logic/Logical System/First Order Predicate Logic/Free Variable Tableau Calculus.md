---
uni-module: "AI"
---

# Free Variable Tableau Calculus

The [[Free Variable]] tableau [[Inference Rule|Calculus]] $\mathcal{T}^f_1$ extensds the [[Analytical Tableaux|Propositional Tableau Calculus]] with the quantifier rules:

![[Bildschirm­foto 2023-01-31 um 11.37.47.png]]
Here in the first rule we postpone the decision by using a **meta-variable** $Y$.

Now in the generalized cut rule we need to take the costs of postponing the decision by checking for the truth values and the substitution equivalence.

![[Bildschirm­foto 2023-01-31 um 11.38.18.png]]

which instantiates the whole tableau by $\sigma$

Now the question is, how can we find the substitution $\sigma$. This is done using First-Order Unification.

The advantage of this calculus compare to the [[Standard Tableau Calculus]] is that no guessing is necessary in the $\mathcal{T}^f_1\forall$ rule.

We have two more derivable rules for the [[Existential Quantifier]]:

![[Bildschirm­foto 2023-01-31 um 11.40.02.png]]

Finitely branching, [[Soundness|sound]] and [[Completeness|complete]] [[First-Order Predicate Logic]].

## Example

We want to prove that $A$ is red.
So we first use our hypothesis/assumptions and try to make them true while we try to make red(A) false. These are the first three lines of the Tableau proof.

The first step mis to apply the [[Universal Quantifier]] elimination rule in which case we introduce the meta variable $Y$. So we postpone the choice of a concrete variable until later.

Then we can apply the usual [[Analytical Tableaux|Propositional Tableau Calculus]] rules to branch on the [[Implikation|implication]] by [[Implikation|implication]] elimination.

We are now in the left branch where we have to make block(Y) false. This is the moment where we have enough information to find a substitution for $Y$ which will close the branch (we choose $A$ as substitute).
This substitiution has to be applied to the whole tableau know. Thats why in the right branch we have red(A). This of course directly closes the right branch.
We thus have a closed tableau and we know that with the assumptions, our formula is valid and thus true for every possible assignment.

![[Bildschirm­foto 2023-01-31 um 12.19.29.png]]
