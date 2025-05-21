---
uni-module: "AI"
---

# Hilbert Calculus

A [[Inference Rule|Calculus]] $\mathcal{H}^0$ consisting of the [[Inference Rule|Inference Rules]]:

$$
\begin{prooftree}
\AxiomC{}
\RL{K}
\UIC{$P\to Q \to P$}
\end{prooftree}
$$

$$
\begin{prooftree}
\AxiomC{}
\RL{S}
\UIC{$(P \Rightarrow Q \Rightarrow R) \Rightarrow(P \Rightarrow Q) \Rightarrow P \Rightarrow R$}
\end{prooftree}
$$

$$
\begin{prooftree}
\AxiomC{$A\Rightarrow B \quad A$ }
\RL{MP}
\UIC{B}
\end{prooftree}
$$

→ Modus Ponens

$$
\begin{prooftree}
\AxiomC{A}
\RL{Subst}
\UIC{$[\mathrm{B} / X](\mathrm{A})$}
\end{prooftree}
$$

→ Substitution
