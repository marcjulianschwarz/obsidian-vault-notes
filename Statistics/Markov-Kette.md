---
uni-module: StochMod
aliases:
  - markov model
  - markov chain
  - Markov Chain
---

# Markov-Kette

A [[Markov Process]] with 1-order [[Markov Property]]. A Markov chain is called **stationary** when its [[Übergangsmatrix|Transition Model]] is independent of time. So the probability to get from the previous step to the next step is equal at every time step.

Eine Folge an [[Zufallsvariable|Zufallsvariablen]], die auf einen [[Zustandsraum]] abbilden, zusammen mit einer [[Anfangsverteilung]] und [[Übergangsmatrix]] heißt Markov-Kette, wenn gilt:

$$P(X_0=S_{i_0},...,X_n=S{i_n})=\nu_{i_0}\hspace{5px}p_{i_0,i_1}...p_{i_{n-1},i_n}$$
Diese Gleichung beschreibt die [[gemeinsame Verteilung]] der Zufallsvariablen, denn für sie gilt nach Rechnung tatsächlich, dass die Summe der Wahrscheinlichkeiten aller möglichen Pfade 1 ergibt und sie immer positiv ist.
Man nennt diese Wahrscheinlichkeiten auch Pfadwahrscheinlichkeiten.

→ [[Hidden Markov Model]]

## Markov-Eigenschaft

[[Gedächtnislose Verteilung]]
