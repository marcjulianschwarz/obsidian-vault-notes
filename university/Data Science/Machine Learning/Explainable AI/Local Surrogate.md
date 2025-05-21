---
uni-module: "XAI"

alias: ["LIME", "Local Interpretable Model-Agnostic Explanations"]
---

# Local Surrogate

Used to explain _individual_, _local_ predictions of a [[Black Box Model]] (thus [[Model-Agnostic]]).

> [!NOTE]+ Idea
> Locally approximate a [[Black Box Model]] via a simpler [[Ante-Hoc|intrinsicly]] interpretable model. Then generate [[Local Explanation|local explanations]] from that model.

In contrast to [[Global Surrogate]] models local surrogate models don't try to explain the global prediction behavior of a model but want to explain why a model made a certain prediction.

## How to train local surrogate models

1. Sample pertubated datapoints and predict with [[Black Box Model]]
   1. by pertubating the datapoint itself
   2. by sampling from [[Normalverteilung|Normal Distribution]] with [[Arithmetic Mean|Mean]] and [[Varianz|Variance]] estimated from the dataset
      1. could also sample from other distributions or just densly sample from feature space with a grid
2. Weigh each datapoint by its [[Proximity]] to the datapoint of interest
   1. by adding it multiple times to the dataset
   2. by weighing it in a model
3. Train an [[Ante-Hoc|Intrinsic]] interpretable model on this weighted dataset
   1. for example [[Lasso Regression|LASSO]], [[Ridge Regression]], [[Decision Tree]]
      1. using models with [[Regularisation]] makes a lot of sense to get simpler models which are easier to explain
      2. Make sure that we have high local [[Fidelity]]
4. Explain the datapoint by interpreting the global behavior of this new model

### Mathematically

$$\operatorname{explanation}(x)=\arg \min _{g \in G} L\left(f, g, \pi_x\right)+\Omega(g)$$
Out of all explanations (models) $G$, find the one $g$ that minimizes the resulting explanations complexity (e.g. via [[Lasso Regression|LASSO]]) and the local loss function $L$ around the neighborhood $\pi_x$ where $f$ is the complex [[Black Box Model]].

### Visually

![[Bildschirmfoto 2023-07-18 um 09.19.07.png]]

- A → [[Black Box Model]]
- B → Sample pertubated datapoints ([[Normalverteilung|Normal Distribution]])
- C → Weigh datapoints based on [[Proximity]] to point of interest
- D → Train [[Ante-Hoc|Intrinsic]] interpretable model

- Model must have high [[Fidelity]] **locally** (it should match the black box predictions)
  - assess with [[Accuracy]] of the interpretable model on the weighted dataset
  - global fidelity can be computed when predicting on the original dataset
- What is a good [[Proximity]] measure and how broad should the neighborhood be?

> [!CHECK] Pros
>
> - [[Model-Agnostic]]
> - human-friendly
>   - [[Selectivity|selective]] (short) explanations
>   - possibly [[Contrastive]]
> - **works for all data types **
> - [[Fidelity]] measure
> - very easy to use
> - can use interpretable features while the [[Black Box Model]] does not

> [!WARNING] Cons
>
> - definition of neighborhood is a big problem
>   - have to try different kernels and look for best explanations
>   - [[Curse of Dimensionality]], proximity measures can become useless in higher dimensions
> - sampling can lead to unlikely datapoints just like in [[Partial Dependence Plot|PDP]]
> - complexity of model has to be defined in advance
> - instability of explanations because of stochastic sampling
>   - difficult to trust explanations
> - can be manipulated by data scientists
