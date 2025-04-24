---
uni-module: AI
aliases:
  - DBN
---
# Dynamic Bayesian Network

A [[Bayesian Network]] $\mathcal{D}$ is called **dynamic** iff its [[Zufallsvariable|Random Variables]] are indexed by a time structure. 

$\mathcal{D}$ is
- time sliced, which means time slices are isomorphic
- a stationary [[Markov-Kette|Markov Chain]]

- Every [[Hidden Markov Model|HMM]] is a single-variable DBN 
- Every discrete DBN is an HMM 
- DBNs have sparse dependencies 

## Exact Inference 

Unrolling the network and running an exact algorithm on the unrolled network. 

![[CleanShot 2023-10-02 at 15.15.41@2x.png]]

- Rollup filtering

