---
uni-module: "AI"

alias: ["Propositional Natural Deduction Calculus", "Natürliches Schließen"]
---

# Natural Deduction

A [[Inference Rule|Calculus]] $\mathcal{ND}_0$ which tries to mimic human argumentation for theorem proving.
It uses these [[Inference Rule|Inference Rules]] to introduce and eliminate connecitves:

![[Bildschirm­foto 2022-12-19 um 09.56.03.png]]

For the [[Implikation|implication]] introduction rule we use a [[Local Hypothesis]] $A$ which we use to derive $B$ by natural deduction. We then **discharge** the local hypothesis by introducing the [[Implikation|implication]]. This mode of reasoning is also called **Hypothetical Reasoning**.

We also write $\mathcal{H} \vdash_{\mathcal{ND_0}} \mathrm{C}$ when there is a natural deduction derivation tree whose leaves are in the **assumptions** $\mathcal{H}$ and the root is the **conclusion** $C$.

If we have some assumptions and the assumption $A$ we can conclude $B$ if and only if we can conclude $A\rightarrow B$ from the assumptions.

Some more [[Inference Rule|Inference Rules]]:
![[Bildschirm­foto 2022-12-19 um 09.57.53.png]]
