---
uni-module: AI
aliases:
  - Prediction
---
# Markov Prediction

A type of [[Markov Inference]] for predicting future state distributions without new evidence. 
$$P(X_{t+k}\mid e_{1:t})$$
Prediction is [[Markov Filtering|Filtering]] without new evidence, so the proof for the next formula is the same.

$$\mathrm{P}\left(\mathrm{X}_{t+k+1} \mid \mathrm{e}_{1: t}\right)=\sum_{\mathrm{x}_{t+k}} \mathrm{P}\left(\mathrm{X}_{t+k+1} \mid \mathrm{x}_{t+k}\right) \cdot P\left(\mathrm{x}_{t+k} \mid \mathrm{e}_{1: t}\right)$$
