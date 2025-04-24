---
uni-module: "MBNN"
---
# Abridged HCNN

In technical applications it might not be possible to unfold an [[Historical Consistent Neural Network|HCNN]] across the whole history. We thus want to only choose a certain [[Memory Length]]. It has to be at least double the length of the forecast horizon. The final network should be applicable to new forecasts (not only on the current history) without retraining.

## Learning

Learning is only done in the [[Architectural Teacher Forcing]] part of the network. It aligns the windows to the target series in the hidden state.

[[Partial Teacher Forcing]] would only degrade the alignment. Thus if you still want to use it you have to extend the past unfolding.

## Initial State 

For [[Abridged HCNN|abridged HCNNs]] you must also use [[Adaptive Uniform Noise]] for the initial state to harden the model against this unknown state.  We can always include future information by adding a second matrix $B$ that has the weights for external factors that we can use for future forecasts. 