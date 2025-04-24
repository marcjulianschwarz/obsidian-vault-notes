---
uni-module: "AI"
---

# Transition Model

A function that assigns to any [[Action]] $a\in \mathcal{A}$ and a state $s\in \mathcal{S}$ a **set of successor states** (here into the set of all possible state combinations [[Potenzmenge]]).
$$\mathcal{T}: \mathcal{A} \times \mathcal{S} \rightarrow \mathcal{P}(\mathcal{S})$$
Updates the [[Belief State]] based on an [[Action]].
