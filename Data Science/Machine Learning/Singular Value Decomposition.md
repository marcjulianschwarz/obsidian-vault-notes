---
uni-module: EMD
---

# Singular Value Decomposition (SVD)

Singular Value Decompositions exist for every matrix, even for non-quadratic matrices and is more efficien than normal eigenvalue decomposition.
It is defined like this:
$$M = U\Sigma V^*$$
Where $U$ is a unitary matrix, $V^*$ is an adjoint matrix and $\Sigma$ is a diagonal matrix with the singular values on its diagonal.
The singular values squared are the eigenvalues of the matrix $M$.

## Berechnung

Man kann die SVD mit zwei Methoden ausrechnen, bei beiden muss man mehr oder weniger die gleichen Sachen auf eine Matrix anwenden:

1. $AA^T$
2. $A^TA$

---

1. Charakteristisches Polynom bestimmen
2. Eigenwerte berechnen
3. Eigenvektoren zu den Eigenwerten berechnen
   1. Normalisieren
   2. Orthogonalisieren
4. U oder V bestimmen
5. Sigma bestimmen
