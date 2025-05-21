---
uni-module: "MBNN"

alias: "PTF"
---

# Partial Teacher Forcing

PTF is [[Dropout]] for [[Historical Consistent Neural Network|HCNNs]]. It is simulating missing data by randomly suppressing elements from the [[Time Series Data]] in the [[Architectural Teacher Forcing]] part.
So the model needs to learn how to replace this missing data with its internal representations.

Also this allows a stochastic learning on only one training example (which is the case for [[Historical Consistent Neural Network|HCNNs]]).

![[Bildschirm­foto 2023-05-30 um 16.22.29.png]]

![[Bildschirm­foto 2023-05-30 um 16.23.16.png]]
