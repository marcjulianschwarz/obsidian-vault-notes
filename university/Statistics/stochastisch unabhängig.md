---
uni-module: "StochMod"

alias:
  [
    "paarweise stochastisch unabhängig",
    "independent",
    "Independence",
    "stochastically independent",
    "Stochastic Independence",
  ]
---
# Stochastische Unabhängigkeit

Zwei [[Ereignis|Ereignisse]] heißen stochastisch unabhängig, wenn gilt:
$$
\begin{equation}
P(A \cap B)=P(A) \cdot P(B)
\end{equation}
$$
Eine ganze Familie an Ereignissen ist unabhängig, wenn für jede Teilmenge eines Index gilt, dass die Wahrscheinlichkeit des Schnitts der [[Ereignis|Ereignisse]] zu dieser Teilmenge an Indexen das Produkt der Wahrscheinlichkeiten ergibt, also:

$$
\begin{equation}
P\left(\bigcap_{i \in J} A_{i}\right)=\prod_{i \in J} P\left(A_{i}\right)
\end{equation}
$$

Wenn diese Bedingung nur für $|J| = 2$ gilt, dann ist die Familie **paarweise** stochastisch unabhängig.
$$\mathbb{P}\left(X_1 \in I_1, \ldots, X_n \in I_n\right)=\mathbb{P}\left(X_1 \in I_1\right) \cdot \ldots \cdot \mathbb{P}\left(X_n \in I_n\right)$$

Let there be a sequence of random variables that are independent. Then the real random variable $f(X_1, \dots, X_k)$ is independent with the rest $X_{k+1},\dots,X_n$.
