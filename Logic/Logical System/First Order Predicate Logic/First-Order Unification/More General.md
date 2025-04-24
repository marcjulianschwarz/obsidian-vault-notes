---
uni-module: "AI"
---

# More General

Let $\sigma$ and $\theta$ be substitutions and $W\subseteq \mathcal{V}_l$ a subset of variables. We say that $\sigma$ is **more general** than $\theta$ :
$$\sigma\leq\theta[W]$$ iff there is a substitution $\rho$ such that
$$\theta=(\rho \circ \sigma)[W]$$ where $\sigma=\rho[W]$ iff $\sigma(X)=\rho(X) \forall X\in W$.

In other words a substitution $\sigma$ is more general than the substitution $\theta$ when we can get to $\theta$ by further substitution in $\sigma$.

We do the restriction on $W$ because thats what is needed to prove all of this xD.

Also see:

- [[Most General Unifier]]
