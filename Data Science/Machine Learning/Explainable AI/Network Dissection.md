---
uni-module: "XAI"
---

# Network Dissection

Tries to answer the question whether a [[Neural Network]] actually understood the concepts that can be visualized with [[Activation Maximization]].
So it quantifies the [[Explainability|Interpretability]] of a [[Unit]].

[[Disentangled Features]]

1. Get images with human-labeled visual concepts
2. Measure the [[Convolutional Neural Network|CNN]] channel activations for them
3. Quantify the alignment of activations and labeled concepts

![[Bildschirmfoto 2023-07-23 um 19.59.14.png]]

## Alignment

_Intersection over Union_
$$I o U_{k, c}=\frac{\sum\left|M_k(x) \bigcap L_c(x)\right|}{\sum\left|M_k(x) \bigcup L_c(x)\right|}$$
