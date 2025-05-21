
# Nested Cross Validation

Use [[Grid Search]] with [[K-Fold Cross Validation]] for two folds, then use the best model with [[K-Fold Cross Validation]] for five more folds. 

So you use a nested cross validation loop to estimate the [[Hyperparameters]] and then evaluate the best model again. The resulting value can be used to compare between the best models with different model architectures. 

For example to compare [[Support Vector Machine|SVM]] with [[Decision Tree]].

