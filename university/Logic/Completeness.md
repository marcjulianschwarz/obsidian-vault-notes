---
uni-module: "AI"

alias: "Vollständigkeit"
---

# Completeness

$$\Phi \models \psi \Rightarrow \Phi \vdash \psi$$

A [[Inference Rule|Calculus]] is called **complete** when given a formula $A$ [[Entailment|entailing]] $B$ can be used to derive $B$.

So whenever $A\models B$ we also have $A\vdash_{\mathcal{C}}B$.

In the sense of an [[Evaluation Criteria for Knowledge Representation]]:

- Can I do all the inferences that I want to do
- Can I do reasoning with incomplete knowledge
