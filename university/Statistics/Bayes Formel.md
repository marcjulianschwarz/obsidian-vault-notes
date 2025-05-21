---
uni-module: StochMod
aliases:
  - Bayes Formula
  - Bayes Rule
---
# Bayes Formel

$(\Omega, \mathcal{A}, P)$ [[Wahrscheinlichkeitsraum|W-Raum]] und $A,B$ [[Ereignis|Ereignisse]] aus $\mathcal{A}$ und $P(A)>0$ und $P(B)>0$.
$$P(A|B)=\frac{P(B|A)P(A)}{P(B)}$$

- [[Prior Probability|Priors]] are simple to compute / find 
	- "diagnosis example" causal relation
		- robust and good to assess 
			- cavity pandemic, one is stable the other changes 
	- **causal** vs **diagnostic**
		- $P(\text{symptom}\mid \text{cause})$ → causal 
		- $P(\text{cause}\mid \text{symptom})$ → diagnostic
		- causal easy to assess 
		- diagnostic ones are actually needed 
		- is A caused by B or B caused by A 
			- diagnostic, liking food doesnt make you a dog 
			- causal, liking food may be caused by being a dog 
