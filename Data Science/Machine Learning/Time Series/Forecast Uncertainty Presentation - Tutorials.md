---
uni-module: "MBNN"
---
# Forecast Uncertainty Presentation - Tutorials

Risk Estimation from [[Feed-forward Neural Network]] to [[Recurrent Neural Network]].

## Approaches to Model Uncertainty

How can we describe Model Uncertainty:

**Approach 0**
Variance of the target series.

More on this approach:
Aleatoric and epistemic uncertainty

- https://towardsdatascience.com/aleatoric-and-epistemic-uncertainty-in-deep-learning-77e5c51f9423
- https://arxiv.org/pdf/1703.04977.pdf
- https://elib.dlr.de/139306/1/igarss2020_tex.pdf

**Approach 1**
Build a forecast model. Use the error as an indicator of the uncertainity in the form of additive noise.

**Approach 2**
Diffusion process (random walk). The channel widens over time.

Approaches 1 and 2 will fail too as we train to zero error. We would thus have zero model uncertainity when our model is trained ==(but only for the past time not the future???)==.

**Approach 3**

Given a _finite_ set of data, there exist _many_ perfect models of the past data, showing different future scenarios caused by different estimations of the hidden states.
So the model will of course **not** be perfect for the future.
This approach obviously describes the model uncertainty.

What about **forecast** uncertainity?

→ Conjecture for large recurrent neural networks.

Every ensemble member is a reasonable forecast given the past observations and prior information. An ensemble (which needs to be large enough) should contain _all_ black swans.

Distributions are independent of

- Ensemble size (if large enough)
- Size of large RNNs

### Size Matters

#### Simple Models

- are easier to interpret ([[Explainable AI|XAI]])
- but may not capture all the complexity of the underlying system
  - leading to higher forecast uncertainty

#### Complex Models

- are harder to interpret and may suffer from overfitting (train to zero error a problem here?)
- better capture the underlying complexity
  - resulting in more stable predictions

How do I find the best tradeoff between model complexity, model [[Explainability|Interpretability]] and forecast uncertainty?

Strucutral → Distribution of the interaction weights

**Functional**
Behavior of the state variables
To determine whether a given model of the world is complex enough to capture all relevant ... we can look at the ...

If the state variables exhibit complex (i.e. non-linear) dynamics, it may suggest that the network is ...
An example where this would not be the case is when the state variables are constant or only show linear behavior.

When we observe this non-complex behavior we might want to choose a more complex model.
