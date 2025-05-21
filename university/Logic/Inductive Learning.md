---
uni-module: AI
---
# Inductive Learning

The **inductive learning problem** $\mathcal{P}:=\langle\mathcal{H}, f, \approx\rangle$ is made up of a 
- [[Hypothesis Space]] $\mathcal{H}$ 
- the to be found hypothesis $h\in \mathcal{H}$
- and a consistent training set $f$ of examples ($x,y$ pairs)

We want to find the hypothesis $h$ such that 
$$f \approx\left(\left.h\right|_{\operatorname{dom}(f)}\right)$$
which means we want to find a function $h$ that is on the domain of $f$ roughly equal to $f$. 

For inductive learning we assume 
- no prior knowledge
- [[Deterministic Environment|deterministic]] [[Fully Observable Environment]]
- examples are given 
- the [[Rational Agent|Agent]] wants to learn $f$

## Consistency and Simplicity 

[[Ockhams Razor]]
![[CleanShot 2023-09-30 at 11.20.25@2x.png]]
![[CleanShot 2023-09-30 at 11.20.34@2x.png]]
![[CleanShot 2023-09-30 at 11.20.46@2x.png]]

![[CleanShot 2023-09-30 at 11.20.57@2x.png]]
