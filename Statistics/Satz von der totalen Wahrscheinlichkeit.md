---
uni-module: "StochMod"

alias: "Marginalization"
---

# Satz von der totalen Wahrscheinlichkeit

Relatively big sums to get the probability of $X$ via dependent probabilities of $X$ with some $Y$.
$$P(X)=\sum_{y\in Y}{P(X,y)}$$


Es sei eine Folge an [[Ereignis|Ereignissen]] $B$, die eine disjunkte Zerlegung vom [[Grundraum]] darstellt, das heißt die Vereinigung dieser [[Ereignis|Ereignisse]] ergibt den [[Grundraum]]. Außerdem sei ein [[Wahrscheinlichkeitsraum|W-Raum]] für den die Folge in der [[Sigma Algebra]] ist.
Dann kann man die Wahrscheinlichkeit eines Ereignises $A$ durch die bedingten Wahrscheinlichkeiten ausrechnen, indem man folgende Summer bildet:

$$
\begin{equation}
P(A)=\sum_{i \in N} P(A \mid B_{i}) P(B_{i})
\end{equation}
$$

Auch alle $B_i$ s müssen zusammen $1$ ergeben.
