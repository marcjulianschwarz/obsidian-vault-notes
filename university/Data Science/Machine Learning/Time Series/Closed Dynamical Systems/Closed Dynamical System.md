# Closed Dynamical System

It is implausible that the world is modelled with 3 matrices. So instead we want to rewrite the [[Recurrent Neural Network]] with only one learnable matrix. By doing this the learning of the model becomes way easier because one doesn't have to think about different learning speeds of the three matrices. 

**Equations**
$$\begin{aligned}
& \boldsymbol{s}_\tau=\tanh \left(A s_{\tau-1}+\left[\begin{array}{c}
0 \\
0 \\
\mathrm{Id}
\end{array}\right] u_\tau\right) \\
& y_\tau=\left[\begin{array}{lll}
I d & 0 & 0
\end{array}\right] s_\tau \\
& \sum_{\tau=1}^T\left(y_\tau-y_\tau^d\right)^2 \rightarrow \min _A
\end{aligned}$$
**Architecture**

![[Bildschirm­foto 2023-04-18 um 10.10.09.png]]

We notice that there is an inconsistency between the past and future modelling as external factors are not available in the future. For normal [[Recurrent Neural Network|RNNs]] we used the [[Error Correction Neural Network|ECNN]] approach to mitigate this issue. 
Now we are combining the target with the external factors and let the model predict or train to predict both the target and the external factor such that we can use the predicted external factor for future predictions. 

Another way to get around this would be to use a **historical consistent** network like an [[Historical Consistent Neural Network|HCNN]] which does not rely on the external factors. 
The model is unfolded along the entire history, so there is only one training example. 

## State Space Dimension & Sparsity of the Transition Matrix


To avoid numerical explosions in large [[Recurrent Neural Network|RNNs]] we need [[Sparsity]].

For [[Historical Consistent Neural Network|HCNNs]] or large [[Recurrent Neural Network|RNNs]] we know by experience 
$$\operatorname{sparsity}(A) \approx \frac{50}{\operatorname{dim}(s)}$$
So we need systems with around 50 nonzero weights per column to make [[Backpropagation]] learn. 

Observing the start vector:
- U-shaped for low sparsity (many alive weights)
- Distribution of start state should be similar to all of the other states 
	- it is not 
	- caused by too extensive error flow in [[Backpropagation]]

### Find good state space dimension:

1. Start with enough dimensions for the state 
2. Enforce sparsity such that the distribution of the start vector is flat 
3. If the final error is not small enough → increase dimensions and try again 

> [!IMPORTANT] By experiments
> Ensemble Solutions are Independent of the Sparse Matrix Initializations.
> So if the matrix **is** sparse, it doesnt matter how the sparsity is enforced. The ensemble variation only depends on the random initialization of the weights. 

[[Historical Consistent Neural Network|HCNNs]] are overparamaterized, we thus need to use an [[Ensemble Method|Ensemble]] to narrow down the diffusion process of the individual models. 

## The Long Memory Problem for HCNNs 

[[Lorenz Attractor]]

[[Sparsity]] of the state matrix can also be seen as a trade-off between memory and computational power. 

- Vanilla HCNNs 
- Ensemble of Vanilla HCNNs 
- Large Sparse Transition Matrix HCNN 
- Small Fully Connected Matrix with [[Long Short Term Memory Network|LSTM]]
	- We let the model decide whether it wants to use the LSTM memory or the sparsity memory via the switch-matrix D 
	- After training we can see we mostly have sparsity memory and nearly no LSTM memory 
- [[Partial Teacher Forcing]]
	- best results on the [[Lorenz Attractor]]

Other examples of deterministic but chaotic dynamical systems 
- The Rabinovich-Fabrikant system 
- The Rossler system 

[[Homotopy for PTF]]

## Sensitivity Analysis & Feature Selection 

How many observables do we have to use in an HCNN? 
Trade-off between large window to the world (good for forecasting) versus small window in the wold (easier to predict observables).

[[Sensitivity Analysis]] for one observable. Here we show the absolute value for the derivation of one observable to all inputs. 

![[Bildschirm­foto 2023-05-30 um 16.38.29.png]]

**Observation**: The sensitivities between forecasts and present time observations is unexpectedly increasing over time.

**Explanation**: The above observation is an artefact: the large / sparse state transition matrix causes a slow interaction of the information flows in the network.

1. Find relevant causalities via [[Sensitivity Analysis]]
2. Skip support variables that explain the task very well but are hard to be forecasted themself by looking at the error. 
