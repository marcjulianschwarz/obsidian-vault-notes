---
uni-module: AI
aliases:
  - BN
  - Bayesian Networks
  - Belief Network
  - Probabilistic Network
  - Bayesian Net
---
# Bayesian Network

## Introduction 

Using the [[Joint Probability Distribution|Full Joint Probability Distribution]] introduces
- $k^n$ number of probabilities 
- computational cost of dealing with this size 
- impossible to assess all of these probabilities

Instead, we want to exploit [[stochastisch unabhängig|Independence]] together with [[Posterior Probability|Conditional Probability]] so that we can leave out the independent parts in the [[Joint Probability Distribution|Full Joint Probability Distribution]] via 
$$P(a \mid b)=P(a)$$
and adding these probabilites back in after the fact using the [[Prior Probability]]. 

Some Probabilistic Reasoning tools and ideas needed to talk about a [[Bayesian Network]] are:
- [[Probability Product Rule]]
- [[Probability Chain Rule]] 
- [[Satz von der totalen Wahrscheinlichkeit|Marginalization]]
- [[Probability Normalization]]
- [[Bayesian Computation Rule]]
- [[Bayes Formel|Bayes Rule]]
- Multiple Evidence 
	- Apply [[Probability Normalization|Normalization]] $P(X\mid e)=\alpha P(X, e)$
	-  then [[Probability Product Rule|Product Rule]] $P(X, e)=P(e\mid X)\cdot P(X)$
- [[Conditional Independence]]
- [[Naive Bayes Classifier]]

Given multiple evidence we can exploit [[Conditional Independence]].

One can do inference on [[Bayesian Network|Bayesian Networks]] either by exact enumeration or by [[Variable Elimination]].

## Definition

- a [[Graph]] ([[Directed Acyclic Graph|DAG]]) or [[Network]] of causal dependencies 
- a methodology for representing the [[Joint Probability Distribution|Full Joint Probability Distribution]] in a compact way 
- depicts [[Conditional Independence]] relations of [[Zufallsvariable|Random Variables]]
- [[Probabilistic Reasoning]] can exploit this structure for improved efficiency 
- optimized database of the [[Joint Probability Distribution|Full Joint Probability Distribution]]
	- can be queried for probabilities with given evidence (see inference)

## Designing a Network

1.  Define [[Zufallsvariable|Random Variables]] fitting to the domain
2. Identify their dependencies
3. Order causes before symptoms
4. Create [[Graph]]
5. Insert Conditional Probability Tables (CPTs)

## Recovering Probabilities 

We can recover probabilities for a given state or realisation of the random variables of the network with 
$$\mathrm{P}\left(X_1, \ldots, X_n\right)=\prod_{i=1}^n \mathrm{P}\left(X_i \mid \operatorname{Parents}\left(X_i\right)\right)$$
where all probabilites are given in the CPTs of the network. 

## Probabilitistic Inference on a Bayesian Network

We want to know the probabilities for a set $X$ of **query variables** under the **evidence** given by the [[Ereignis|Event]] $e$ of **evidence variables** $E\subseteq X$  
$$P(X\mid e)$$
with the **hidden variables** $Y=\set{X_1, ..., X_n}\setminus X \cup E$.  

We will reformulate this using [[Probability Normalization|Normalization]] to 
$$P(X\mid e)=\frac{P(X\land e)\cdot P(X)}{P(e)}=\alpha\cdot 
P(X,e).$$
If we have hidden variables we need to additionaly [[Satz von der totalen Wahrscheinlichkeit|marginalize]] over them, so we get
$$P(X \mid e)=\alpha\left(\sum_{y \in Y} P(X, e, y)\right).$$
Now $\alpha$ can be easily calculated.

To get $P(X,e)$ we first order all random variables and the evidence in the order of the network and then apply the [[Probability Chain Rule|Chain Rule]] 
$$P(X_1,...,e)=P(e|...)\cdot ... \cdot P(X_1)$$
Here we exploit the structure of the [[Network]] to only work with the [[Conditional Independence|conditional independencies]] by only looking at the parents of $X_i$
$$P(X_i\mid \text{Parents}(X_i))$$
In the end we have sums of products of conditional probabilities from the bayesian network. 
![[CleanShot 2023-09-27 at 20.41.56@2x.png]]

We could just calculate this [[Expression Tree]] using [[Depth-first search]] but the [[Laufzeit|Running Time]] would be exponential in the number of hidden variables that we have.
$$\mathcal{O}(2^{\#(Y)})$$
Instead we can use [[Variable Elimination]] that avoids this.
Other methods are 
- Inference by sampling 
- Clustering 
- Compilation to [[Erfüllbarkeitsproblem der Aussagenlogik|SAT]] and using SAT Solver 
- Dynamic Bayesian Network 
- Relational Bayesian Network 
- First-order Bayesian Network (BLOG language)

## Size

How many numbers are there in the CPTs or what is the **compactness** of the network? 
$$\operatorname{size}(\mathcal{B}):=\sum_{i=1}^n \#\left(D_i\right) \cdot \prod_{X_j \in \operatorname{Parents}\left(X_i\right)} \#\left(D_j\right)$$

**Deterministic Nodes** 

Canonical Distributions = standard patterns that CPTs follow #question 

A node is called **deterministic** if its value ic completely determined by the value of its parents as they are then modelled by direct causal relationships.

- logical dependencies 
- numerical dependencies 

![[CleanShot 2023-10-02 at 11.23.07@2x.png]]

- Leak Node 

Noisy Disjunction Node (Noisy-OR)
$$\mathrm{P}\left(X_i \mid \operatorname{Parents}\left(X_i\right)\right)=1-\prod_{\left\{j \mid X_j=\mathrm{T}\right\}} \boldsymbol{q}_j$$
So we bascially have 
$$P(X\mid A,\neg B,C)=\dots$$
where we assign probabilities to $X$ happening because of the true factors on the right side. 

