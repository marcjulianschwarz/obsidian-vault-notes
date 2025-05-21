---
uni-module: AI
---
# Decision List


Like [[Decision Tree]] but with restricted branching, but more complex tests.

Given arbitrary size they can represent arbitrary boolean functions.

**Example**

![[CleanShot 2023-10-04 at 11.51.18@2x.png]]

This is a 2-DL because it has tests of at most 2 literals. This list contains the set of [[Decision Tree|decision trees]] with depth of at most 2. 

## Learning 

![[CleanShot 2023-10-04 at 11.57.20@2x.png]]

**Intuition**
When there are no examples return the trivial list of only *No*.
Find a test (formula) that matches a subset of the examples such that there are only all positive or only all negative cases. Label that test with Yes and No accordingly.
Now remove the examples from the set and recursively call the algorithm again with the remaining samples to get more tests. 

