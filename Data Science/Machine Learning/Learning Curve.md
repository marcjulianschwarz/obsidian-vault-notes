---
uni-module: AI
---
# Learning Curve

A learning curve shows the validation and training [[Accuracy]] for varying sample sizes of training data.

It can be used to tell whether the model is currently [[Overfitting]] or [[Underfitting]] depending on the amount of data that was used to train the model.

![[CleanShot 2023-10-04 at 10.29.07@2x.png]]

The shape of the learning curve shows whether a given problem (target function) is realizable given the [[Hypothesis Space]] that was used for training. 
- non-realizable → hypthesis space too small 
- redundant → data redundancy, useless features, etc. 
- realizable → hypothesis space has right size 

![[CleanShot 2023-10-04 at 10.30.17@2x.png]]

Also see [[Validation Curve]].