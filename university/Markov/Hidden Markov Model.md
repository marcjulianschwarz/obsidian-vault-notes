---
aliases:
  - HMM
uni-module: AI
---
# Hidden Markov Model

A hidden Markov model is a [[Markov-Kette|Markov Chain]] with a single discrete state variable $X_t$ with domain $\set{1,...,S}$ and a single, discrete evidence variable. 

The [[Übergangsmatrix|Transition Model]] 
$$P(X_t\mid X_{t-1})$$
is a single $S\times S$  matrix.

The [[Sensor Model]] 
$$P(e_t\mid X_t=i)$$ is an $S$-vector.

The idea is that we can now formulate [[Markov Inference]] as matrix calculations (which can be sped up by optimized algorithms). 

To make this work we create a diagonal sensor matrix from the [[Sensor Model]] vector. 

**Filtering**
$$\mathrm{f}_{1: t+1}=\alpha \cdot \mathrm{O}_{t+1} T^t \mathrm{f}_{1: t}$$

**Smoothing**
$$\mathrm{b}_{k+1: t}=\mathrm{TO}_{k+1} \mathrm{~b}_{k+2: t}$$






[[Zustandsraum]]
[[Emissionen]]

[[Sensor Model]]
[[Anfangsverteilung]]

## Beispiel Veranschaulichung

![[Bildschirmfoto 2022-03-09 um 20.42.17.png]]
