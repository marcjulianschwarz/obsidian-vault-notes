---
uni-module: "AI"
---

# Deduction

Which statements $B$ can be derived from $A$ using a set $\mathcal{C}$ of [[Inference Rule|Inference Rules]]?
$$A\vdash_{\mathcal{C}}B$$
- [[Sequent Calculus Formulation]]
- [[Natural Deduction]]

## Example

We have a set of [[Inference Rule|Inference Rules]] $\mathcal{C}$ which contains the only rule:

$$
\begin{prooftree}
\AxiomC{}
\AXC{$A\quad A\to B$}
\UIC{$B$}
\end{prooftree}
$$

We can now say that we could use $P$ and $P\to Q$ to derive $Q$:
$$P, P \Rightarrow Q \vdash_{\mathcal{C}} Q$$
or in other words, $Q$ is derivable from $P$ and $P\to Q$ with the set of [[Inference Rule|Inference Rules]] $\mathcal{C}$.
