---
uni-module: StochMod
aliases:
  - Verteilung
  - W-Maß
  - Distribution
  - Probability Measure
  - Probability Function
---

# Wahrscheinlichkeitsmaß

Eine Funktion $P: \mathcal{A}\rightarrow\mathbb{R}$ heißt so, wenn gilt:

1. Die Wahrscheinlichkeit ist immer zwischen 0 und 1
2. Die Wahrscheinlichkeit von $\Omega$ [[Grundraum]], also dass irgendwas passiert ist immer 1
3. [[Sigma-Additivität]]

Bestandteil eines [[Wahrscheinlichkeitsraum]].

## Properties

1. Die Wahrscheinlichkeit der leeren Menge ist null
2. Für paarweise disjunkte Mengen gilt, dass die Wahrscheinlichkeit der Vereinigung dieser Mengen gleich der Summe der einzelnen Wahrscheinlichkeiten entspricht (endlich). Beweis durch [[Sigma-Additivität]]
3. Die Wahrscheinlichkeit vom Komplement eines [[Ereignis]] ist 1 - die Wahrscheinlichkeit des Ereignises
4. Für $A,B$ mit $A \subset B$ gilt $P(B\\A)=P(B)-P(A)$
5. Für $A,B$ mit $A \subset B$ gilt $P(A) \leq P(B)$
6. Für $A,B$ gilt $P(A \cup B)=P(A)+P(B)-P(A\cap B)$
7. Für jede unendliche Folge an Ereignissen gilt,

## Examples

[[Gleichverteilung|Uniform Distribution]]
[[Binomialverteilung|Binomial Distribution]]
[[Bernoulli-Verteilung|Bernoulli Distribution]]
[[Negative Binomialverteilung|Negative Binomial Distribution]]
[[Geometrische Verteilung|Geometric Distribution]]
[[Poisson Verteilung|Poisson Distribution]]
[[Gamma Distribution]]
[[Exponentialverteilung|Exponential Distribution]]
[[Standardnormalverteilung|Standard Normal Distribution]]
[[Dirac-Verteilung]]
