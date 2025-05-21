---
uni-module: "XAI"
---

# Counterfactual


[[Local Explanation]] of changing a datapoint in a minimal way such that it achieves a different predefined output. Often a really good [[Explanation]] which explains what is most important locally. Often [[Model-Agnostic]].

> If X had not occurred, Y would not have occurred

Unlike [[Prototype|prototypes]] , counterfactuals do not have to be actual instances from the training data, but can be a new combination of feature values

- human-friendly

  - [[Contrastive]] → to the current instance via a "what-if" scenario
  - [[Selectivity]] → small number of feature changes

- [[Rashomon Effect]]
  - there are multiple different counterfactuals that all change the prediction equally well
- solve by
  - showing all counterfactuals
  - selecting only the best ones (by some measure)
    - produce the predefined prediction as closely as possible
    - as similar as possible to the original instance regarding feature values
      - [[Manhattan Distance]]
      - [[Gower Distance]]
    - change as few features as possible
    - generate multiple diverse explanations
    - likely feature values (see correlations etc.)

## How to generate counterfactuals

Minimize the [[Loss Function]]
$$L\left(x, x^{\prime}, y^{\prime}, \lambda\right)=\lambda \cdot\left(\hat{f}\left(x^{\prime}\right)-y^{\prime}\right)^2+d\left(x, x^{\prime}\right).$$

- original instance $x$
- current counterfactual $x'$
- predefined output $y'$
- regularisation $\lambda$

Distance between original instance and counterfactual should be minimized
$$d\left(x, x^{\prime}\right)=\sum_{j=1}^p \frac{\left|x_j-x_j^{\prime}\right|}{M A D_j}.$$
Stop when constraint is reached
$$\left|\hat{f}\left(x^{\prime}\right)-y^{\prime}\right| \leq \epsilon.$$
So in total
$$\arg \min _{x^{\prime}} \max _\lambda L\left(x, x^{\prime}, y^{\prime}, \lambda\right) .$$

1. Select instance $x$, desired outcome $y'$, tolerance $\epsilon$ and a low initial value for $\lambda$
2. Sample random instance as initial counterfactual $x'$
3. Optimize loss
4. While constraint is not fullfilled
   1. Increase $\lambda$ (more attention on the constraint part)
   2. Optimize loss
   3. Return counterfactual with minimal loss
5. Repeat 2-4 to generate multiple counterfactuals

> [!CHECK]+ Pros
>
> - clear interpretation
> - two results
>   - counterfactual
>   - what was changed
> - [[Model-Agnostic]] and no access to the data is needed (privacy)
> - works for systems without [[Machine Learning|ML]]
> - easy to implement

> [!WARNING]+ Cons
>
> - Instability via the [[Rashomon Effect]]

## Software

- https://github.com/SeldonIO/alibi
