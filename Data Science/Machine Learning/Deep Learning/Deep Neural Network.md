---
alias: DNN
---
# Deep Neural Network

The [[Perceptron]] is the most basic neural network. With more perceptrons we can create a [[Multilayer Perceptron]] which can handle more complex tasks. A [[Neural Network]] with many of those layers is called a deep neural network. 

To optimize our deep learning model we need a [[Loss Function]] that tells us how good it performs using [[Forward and Backward Pass]].

To reduce the loss we can use [[Gradient Descent]] to find the minimum of the loss function and [[Backpropagation]] to pass the error and [[Gradient]] updates back through the network updating all weights. 


**Applications**
- [[Image Classification]]


> [!NOTE]+ Similarity to brain
> The human [[Gehirn|Brain]] consists of different regions which are all specialized to perform a certain tasks.
> 
> A human [[Nervenzelle|Neuron]] can be stimulated (Input) and when it reaches a certain threshold, the neuron fires ([[Aktionspotenzial|Action Potential]]), triggering a stimulation for the next neuron (Output). With a deep neural network we try to model this behaviour.


