---
uni-module: EMD, ML4ENG
aliases:
  - Steepest Descent Learning
---
# Gradient Descent

Finding a [[lokales Minimum|local minimum]] in a "mountain like" environment.

Gradient descent benefits from [[Z-score|Standardization]] as the weight updates are _fair_ between different features.

## Concrete Algorithms

- [[Full-Batch Gradient Descent]]
- [[Stochastic Gradient Descent]]
- [[Mini-Batch Gradient Descent]]


## Approach:

1. Start with random weights
2. Calculate [[Richtung des steilsten Abstiegs|Direction of Steepest Descend]] (using [[Gradient]])
3. Step in that direction (learning rate)
4. Repeat from step 2

![[CleanShot 2023-10-04 at 12.06.50@2x.png]]

## Algorithm:

1. Calculate loss
2. Calculate the [[Gradient]] of the loss
3. Subtract $\mu$ - times the [[Gradient]] of the loss ($\mu$ = learning rate)
4. Start at step 1

> [!Warning] Cons
>
> - multiple [[lokales Minimum|Local Minima]] will prevent you from finding the [[globales Minimum]] (there is no guarantee to finding an optimal solution)
> - depends on random initialization
> - depends on learning rate:
>   - high values → jumping over the minimum
>   - low values → never reach the minimum

> [!NOTE] 
>  - For each epoch (= one loop over the training data)
  >- For each batch (= one small portion of the training data)
 > 	- Compute the error
> 	 - Compute the gradients
  >	- Update the parameters using the gradients

## Example 

For the [[Mean Squared Error]] [[Loss Function]] we can derive gradient descent updates. 

![[CleanShot 2023-10-04 at 12.09.12@2x.png]]

And for multiple examples we get 

![[CleanShot 2023-10-04 at 12.10.19@2x.png]]

batch gradient descent learning rule for univariate linear regression. 



**The Concept of Batches**
Instead of computing the sum of losses on one complete epoch, which can be very expensive, we divide each epoch into multiple smaller pieces → batches.
Usually the size of these batches is a fixed number.

![[IMG - Batch Process.png]]
