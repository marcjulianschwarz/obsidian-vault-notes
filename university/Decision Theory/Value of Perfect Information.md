---
uni-module: AI
aliases:
  - VPI
---
# Value of Perfect Information

$$\operatorname{VPI}_E(F):=\left(\sum_{f \in D} P(F=f \mid E) \cdot \operatorname{EU}\left(\alpha_f \mid E, F=f\right)\right)-\mathrm{EU}(\alpha \mid E)$$

Given this, the best possible [[Action]] out of all actions $A$ is 
$$\alpha_f=\underset{a \in A}{\operatorname{argmax}} \operatorname{EU}(a \mid E, F=f)$$

When more than one piece of evidence can be gathered this becomes a sequential decision problem.
## Properties 


> [!purple-highlight]+ Non-negative
> In [[Erwartungswert|Expectation]], not [[Post-Hoc]]
> 
> $V P I_E(F) \geq 0$

> [!purple-highlight]+ Non-additive
> For example when obtaining the same information twice, or the new information contains parts of the old information that we already have.
> 
> $V P I_E(F, G) \neq V P I_E(F)+V P I_E(G)$

> [!purple-highlight]+ Order-independent
> It does not matter in what order we gather information. At the point we make the decision, we would still have the same value of information.
> 
> $V P I_E(F, G)=V P I_E(F)+V P I_{E, F}(G)=V P I_E(G)+V P I_{E, G}(F)$




