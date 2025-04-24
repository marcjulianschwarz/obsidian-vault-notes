---
uni-module: "XAI"

alias: "Explanations"
---

# Explanation

Relates the feature values of an instance to its model prediction in a humanly understandable way.

The answer to a _why-question_.

An [[Explainable AI]] method can give **many** explanations for a given model. It is not deterministic but should be stable. Only valid for one specific prediction.
Explanations make a model more [[Explainability|interpretable]].

There exist

- [[Local Explanation]]
- [[Global Explanation]]

## Properties

Higher is better.

- [[Accuracy]]
  - important when using explanations instead of model predictions (e.g. [[Decision Tree]] which approximates a [[Neural Network]])
- [[Fidelity]]
- [[Consistency]]
- [[Stability]]
- [[Comprehensability]]
- Cetainty
- Degree of Importance
- Novelty
- Representativeness
- [[Selectivity]]

## What makes an explanation human-friendly?

See https://christophm.github.io/interpretable-ml-book/explanation.html
