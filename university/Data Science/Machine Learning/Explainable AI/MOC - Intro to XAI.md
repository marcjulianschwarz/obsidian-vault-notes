---
tags:
  - MOC
uni-module: XAI
---
# MOC - Intro to XAI
## General

We differentiate between a [[Black Box Model]] and [[White Box Model]]. We want to be able to generate explanations from a model → [[Explainability|Interpretability]].

> [!NOTE] Problem with Black Box models in science
> The **goal of science** is to gain knowledge, but many problems are solved with big datasets and black box machine learning models. The model itself becomes the source of knowledge instead of the data. Interpretability makes it possible to extract this additional knowledge captured by the model.

### When do we need explainability and what do we gain from it?

In _low-risk environments_ you might **not** need [[Explainability]], e.g.

- no impact
- problem is well studied
- **manipulation is unwanted** (can happen when one can explain the outcome)

You **need** it when

- a correct prediction only partially solves the original problem.
- the task requires safety measures
- you want to detect [[Bias]]
- you need social acceptance (trust)
- you want to manage social interactions
- you want to debug or audit a model

With [[Explainability]] you also **gain**

- Fairness (Loan Rejection)
- Privacy
- Reliability
- Causality (in the models context)
- Trust ([[ChatGPT]])
- [[Action Advice]]

Today, explainable machine learning can also be seen as part of the user experience by providing relevant insights into the model.

## Taxonomy of Interpretability Methods and their Explanations

An interpretation method can either be

- [[Ante-Hoc|Intrinsic]] or [[Post-Hoc]]
- [[Model-Specific]] or [[Model-Agnostic]]

It can generate an [[Explanation]] which can be a

- [[Local Explanation]]
- [[Global Explanation]]

_Averaging_ many local explanations can increase their scope to get global over time.

Its explanations can be

- a Feature Summary (Statistic and or [[Data Visualization]])
  - [[Feature Importance]]
  - [[Partial Dependence Plot]]
  - [[Saliency Map]]
- model internals (only for already interpretable models, so [[Model-Specific]])
  - learned weights
  - [[Decision Tree]]
  - [[Convolution]] Layers (visualized)
- data points (text + images) (could be added to your training [[Dataset]])
  - [[Prototype]]
  - [[Counterfactual]]

[[Bildschirm­foto 2023-05-07 um 13.39.04.png]]
Trade-off between [[Explainability]] and accuracy. Use better image from YouTube video hetter image from YouTube video here. #todo 

[[Bildschirm­foto 2023-05-07 um 14.35.25.png]]

## Scope of Interpretability

- [[Algorithm Transparency]]

Global, Holistic Model Interpretability

- understand the models ouputs based on its inputs, algorithm and internals
- how does the trained model make predictions

Global Model Interpretability on a Modular Level

- how do parts of the model affect predictions
- for example single weights and not all at the same time

Local Interpretability for a Single Prediction

- why was a certain prediction made
- dependence on features (linear, etc.)

Local Interpretability for a Group of Predictions

- use the others above for this

## Evaluation of Interpretability

- [[Application Level Evaluation]]
- [[Human Level Evaluation]]
- [[Function Level Evaluation]]

## Properties of Interpretability Methods

- [[Expressive Power]]
- [[Translucency]]
- [[Portability]]
- [[Komplexitätsklassen|Complexity]]

## Interpretable Models

Properties

- Linearity
  - (between features and target)
- Monotonicity
- Feature-Interaction
  - automatically include feature interactions
- Task
  - [[Regression]] [[Classification]] or both

![[Bildschirm­foto 2023-05-29 um 16.31.38.png]]

### Linear Regression

- [[Linear Regression]]
  - [[Encoding of Categorical Features]]

Sometimes your data might have too many features. So we want to have [[Sparsity|sparse]] Linear Models (with [[Regularisation]]) like

- [[Lasso Regression|LASSO]]
- [[Ridge Regression]]
- [[Elastic-Net Regression]]

You can use [[Feature Selection]] methods to reduce the number of features for a model to make it more interpretable.

### Logistic Regression

See [[Logistic Regression]]

### Other linear regression extensions

When assumptions in [[Linear Regression]] are violated we can use extensions like the [[Generalized Linear Model|GLM]] or [[Generalized Additive Model|GAM]].

Non-gaussion distributions:

- [[Generalized Linear Model]]

Add interactions between features manually.

To get nonlinear effects we can use

- Feature Transformation (e.g. log)
- Feature Categorization / [[Data Discretization]]
- [[Generalized Additive Model]]

These extensions make linear model harder to interpret but increase their performance. Still, [[Random Forest]] or other [[Ensemble Method|Ensembles]] are better most of the time and still easier to interpret.

### Decision Tree

- [[Decision Tree]]
  - [[Classification and Regression Trees]]
- [[Linear Regression]] plus [[Decision Tree]] rules → [[RuleFit]]

## Global Model-Agnostic Methods

Here we look at model [[Model-Agnostic]] methods that explain the global behavior of our model. So they describe the **average behavior** and are expressed as the **expected values** over the data distribution.

| Not example based                                      | Example based           |
| ------------------------------------------------------ | ----------------------- |
| [[Partial Dependence Plot]]                            | [[Counterfactual]]      |
| [[Individual Conditional Expectation Curve]]           | [[Prototype]]           |
| [[Marginal Plot\|M-Plot]]                              | Influential Instances   |
| [[Accumulated Local Effect Plot]]                      | [[K-Nearest Neighbors]] |
| [[Feature Interaction]] via [[Friedman's H-statistic]] |                         |
| [[Permutation Feature Importance]]                     |                         |
| [[Global Surrogate]]                                   |                         |

![[Bildschirmfoto 2023-07-11 um 10.33.07.png]]

## Local Model-Agnostic Mehthods

Here we look at [[Model-Agnostic]] methods that explain some local behavior, mostly an individual prediction, of our model.

Methods (all post-hoc)

- [[Individual Conditional Expectation Curve]]
- [[Local Surrogate]] (LIME)
- [[Counterfactual]]
- [[Shapley Values]]
- [[Shapley Additive Explanations]]

## Neural Network

To interpret [[Neural Network|Neural Networks]] we can use all [[Model-Agnostic]] methods. However it makes a lot of sense to also use specific methods that take advantage of the structure of neural networks like the [[Gradient]] or [[Hidden Layer|Hidden Layers]] which can contain learned features and concepts.

### Learned Features

#### Feature Visualization

[[Activation Maximization]]

- [[Global Explanation]]
- can be [[Model-Agnostic]] when not using [[Gradient|gradients]] (they only make the optimization more efficient)

[[Network Dissection]]

> [!CHECK] Advantages
>
> - automatic linkage between [[Unit]] and concept with [[Network Dissection]]
> - communicate [[Neural Network|Neural Networks]] in a non-technical way
> - concepts beyond the class labels
> - can be combined with feature attribution methods

> [!WARNING] Disadvantages
>
> - many feature visualization images are not interpretabel (no human concept behind them)
> - there are too mayn units to look at
> - no [[Disentangled Features]] in some cases
> - pixel-level segmentation datasets are needed

### Pixel Attribution

[[Saliency Map]]
