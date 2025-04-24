---
uni-module: "MBNN"

alias: "HCNN"
---
# Historical Consistent Neural Network

Another [[Recurrent Neural Network|RNN]] model that uses the entire history as one training example. The model architecture is thus unfolded along this history. It does not need the external factors.

## Universal Approximation

![[Bildschirm­foto 2023-05-30 um 14.11.18.png]]

## Basic Learning of HCNNs

For HCNNs we dont have any [[Hyperparameters]] for the [[Memory Length|Past Horizon]] as it is unfolded along the entire history.
The starting state and the matrix $A$ are all learned together.

One important part of learning HCNNs is [[Architectural Teacher Forcing]] which is kind of like [[Error Correction Neural Network|ECNN]] for HCNNs, so it works with only one learned matrix.

