---
uni-module: "XAI"

alias: ["Saliency Maps", "Pixel Attribution"]
---

# Saliency Map

Sinlge number per feature in the form of a pixel-value. Often visualized as [[Heatmap]] to show which parts of an image are most important to classify it with a [[Neural Network]].

A special type of [[Feature Attribution]].

[[Model-Agnostic]] methods

- [[Local Surrogate|LIME]]

Gradient-based methods:

- [[Vanilla Gradient]]
- [[Grad-CAM]]

Path-attribution methods

- Deep Taylor
- Integrated Gradients
- [[Local Surrogate|LIME]]

Method that creates such an explanation is:

- [[Post-Hoc]]
- [[Saliency Map]] is result (subgroup of [[Feature Importance]])
- Cant tell if [[Model-Agnostic]] or [[Model-Specific]]
- It is a [[Local Explanation]]

![[Bildschirm­foto 2023-05-07 um 15.09.14.png]]

- Not [[Contrastive]]
  - [[Saliency Map]] shows where to look and not why
- It is [[Selectivity]], most of the color is gray
