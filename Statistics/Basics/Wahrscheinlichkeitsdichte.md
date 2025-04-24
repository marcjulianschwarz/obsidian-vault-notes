---
uni-module: "StochMod"

alias: [Dichte, W-Dichte, "PDF", "Probability Density Function"]
---

# Wahrscheinlichkeitsdichte

Ist mehr oder weniger äquivalent zur [[Zähldichte]] im diskreten Fall.

Da wir diese Dichte jetzt aber auf den reellen Zahlen definieren können wir nicht einfach alle Wahrscheinlichkeiten aufsummieren sondern müssen über diese integrieren.

$$\int_{-\infty}^{\infty} f(x) d x=1$$

Eine W-Dichte definiert eindeutig eine [[Wahrscheinlichkeitsmaß|Verteilung]] auf dem [[Grundraum]] $(\mathbb{R},\mathcal{B}(\mathbb{R}))$ durch:
$$P([a, b]):=\int_{a}^{b} f(x) d x, \quad \forall a \leq b, a, b \in \mathbb{R}$$

Anhand dieser Formel kann man auch erkennen, dass es wenig Sinn macht nach der Wahrscheinlichkeit für nur eine Zahl zu suchen. Denn setzt man $a=b$ ergibt sich immer die Wahrscheinlichkeit Null.
Das ist der Grund warum wir in reellen Wahrscheinlichkeitsräumen immer die Wahrscheinlichkeit berechnen, dass eine Zahl in einem gegebenen Intervall ist.

Jede W-Dichte definiert also eindeutig eine [[Wahrscheinlichkeitsmaß|Verteilung]] auf dem [[Grundraum]] mit der [[Borel Sigma Algebra]] über $\mathbb{R}$.

## W-Dichten zu den Verteilungen

[[Gleichverteilung]]
[[Exponentialverteilung]]
[[Normalverteilung]]
[[Standardnormalverteilung]]

### Verteilung, die keine W-Dichte besitzen

[[Dirac-Verteilung]]

Um aber alle [[Wahrscheinlichkeitsmaß|Verteilungen]] auf einem [[Wahrscheinlichkeitsraum|W-Raum]] zu beschreiben gibt es die [[Verteilungsfunktion]].
