---
uni-module: AI
---
# Temporal Probability Model

Has two sets of [[Zufallsvariable|Random Variables]] called 
- state variables that are unobservable
- evidence variables that are observable 

Both variables are indexed by numbers from $\mathbb{N}$.

We can also denote time spans 
$$\mathrm{X}_{a: b}=\mathrm{X}_a, \mathrm{X}_{a+1}, \ldots, \mathrm{X}_{b-1}, \mathrm{X}_b$$

We want to model a [[Temporal Probability Model]] with [[Markov Process|Markov Processes]] that fullfill some [[Markov Property]]. One such model is the [[Markov-Kette|Markov Chain]] which however does not really reflect reality. We could increase the order (which adds more dependencies, bad) or we add more state variables to get more information into the model.

We can now separate the model into the [[Übergangsmatrix|Transition Model]]  (probability for the next step in time) and the [[Sensor Model]] (probability of the evidence for the next step in time).

- [[Sensor Markov Property]]

[[Übergangsmatrix|Transition Model]] and [[Sensor Model]] for a [[Markov-Kette|Markov Chain]] of 1-order [[Markov Property]] and [[Sensor Markov Property]].
![[CleanShot 2023-09-28 at 11.44.29@2x.png]]

If we know the [[Prior Probability|Priors]] we can even calculate the [[Joint Probability Distribution|Full Joint Probability Distribution]]
$$\mathrm{P}\left(\mathrm{X}_{0: t}, \mathrm{E}_{1: t}\right)=\mathrm{P}\left(\mathrm{X}_0\right) \cdot \prod_{i=1}^t \mathrm{P}\left(\mathbf{X}_i \mid \mathbf{X}_{i-1}\right) \cdot \mathrm{P}\left(\mathrm{E}_i \mid \mathrm{X}_i\right)$$
- [[Markov Inference]]
	- [[Markov Filtering|Filtering]]
	- [[Markov Prediction|Prediction]]
	- [[Markov Smoothing|Smoothing]]
	- [[Markov Most Likely Explanation|Most Likely Explanation]]

- [[Hidden Markov Model]]
- Country Dance Algorithm 
- [[Dynamic Bayesian Network]]

