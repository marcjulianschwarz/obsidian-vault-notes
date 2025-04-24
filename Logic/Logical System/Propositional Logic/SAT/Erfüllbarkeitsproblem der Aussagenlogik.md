---
uni-module: "LNS"

alias: "SAT"
---

# Erfüllbarkeitsproblem der Aussagenlogik

Meistens in [[Conjunctive Normal Form]].

Ist in [[Nondeterministic Polynomial Time Complete|NPC]] und exponentiell (worst case) in der Anzahl der Variablen lösbar, zum Beispiel durch das aufstellen einer Wahrheitstabelle.

## Beispiel

$$(A \vee B \vee \bar{C}) \wedge(A \vee B \vee C)$$

$$
\begin{array}{ll}
x_{1}+x_{2}+\left(1-x_{3}\right) \geq 1 & \left(D_{1}=\{1,2\}, E_{1}=\{3\}\right) \\
x_{1}+x_{2}+x_{3} \geq 1 & \left(D_{2}=\{1,2,3\}, E_{2}=\emptyset\right) \\
x \in\{0,1\}^{3} &
\end{array}
$$
