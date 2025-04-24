---
aliases:
  - RNN
  - RNNs
tags:
  - note
  - datascience
---

# Recurrent Neural Network

A [[Neural Network]] which works on [[Time Series Data]].

Past Unfolding → have to figure out yourself
Future Extension → customer

## Architecture

![[Bildschirm­foto 2023-04-16 um 22.35.12.png]]

An alternative formulation that implements long term dependencies is called [[Long Short Term Memory Network]].

[[Time Series Data]] can be decomposed into an _autonomous_ (Eigendynamic) part and an _external driven_ part.

For future predictions we dont have access to the external factors which is why we depend on a **strong eigendynamic** to achieve good long-term predictions. The further we predict into the future the less influence old external factors will have.

## Structure

The size of the [[Hidden Layer]] (state) can get big and complicated. It might need to be pruned with [[Korrelation|Pearson Correlation]] after the training. This means strongly correlated states are redundant and will be removed from the state. One can create a simple test for this which is being evaluated at the present time point in the RNN.

The [[Memory Length]] and the future unfolding is highly dependent on the application the RNN is used for.
Some example times of Siemens were

- 440 day steps (two full years)
- 300 week steps → predict up to 52 weeks

## Basic Learning of small RNNs

We want to make sure that the matrices $A,B,C$ are constant over time. They should only change in each training step. This is why we want to use the special variant of [[Backpropagation]] called [[Backpropagation for Shared Weights]].

Position the architecture randomly along a part of the data series. For every position the pair of inputs/outputs changes and one [[Backpropagation]] learning cycle will be done.

Also we want to always include the future extension in training as it will help to focus more on the eigendynamics which will later allow for longer forecasting.

## Feature Selection

Sometimes we might have too many external factors and want to only focus on the ones that are needed to predict the target variable. We can do [[Feature Selection|Feature Selection]] for RNNs just like for normal [[Neural Network|NNs]] by doing a [[Sensitivity Analysis]] or by training an _inverse model_ in which we try to find which factors are related to the target by checking the various errors in the prediction.

![[Bildschirm­foto 2023-04-14 um 18.12.49.png]]

## State Initialization

Setting the initial starting vector $s_0=0$ postulates an independence from the initial condition which might not be true for every case.
A better starting vector would have some initial noise [[Adaptive Uniform Noise]] that hardens the model against the unknown initial state. The learned matrxix $A$ will over time squeeze out the uncertainty from the beginning.
The noise allows the model to learn the initial state by its own by exploring different possibilities and learning from the [[Residuum|Residual Error]]. Setting it to zero would eliminate this.

We have:
bias → $s_0$ → noise → Id → $s_1$ ...

![[Bildschirm­foto 2023-04-18 um 10.04.38.png]]


## Uncertainty in Forecasting

See [[Forecast Uncertainty Presentation - Tutorials]].

## Other resources

- [Attention and Augmented Recurrent Neural Networks](https://distill.pub/2016/augmented-rnns/)
- Attention Is All You Need 
