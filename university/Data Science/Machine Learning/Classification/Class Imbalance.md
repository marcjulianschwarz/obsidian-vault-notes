---
uni-module: "KDD"
---
# Class Imbalance

When there are more sample from one class than the other. Can lead to poor results in [[Classification]] and [[Regression]] tasks as the rare class hasnt been seen often by the model while training.

Methods to circumvent this for binary classification problems are:

- [[Oversampling]]
- [[Undersampling]]
- SMOTE
- Moving the [[Decision Boundary]] so that rare samples are easier to classify (works for [[Bayesian Classifier]], [[Naive Bayes Classifier]])
- Ensemble techniques

For multiclass problems it is still hard to remove class imbalance artifically without skewing their relation.
