---
uni-module: "KDD"
---
# Classification

Predicts categorical class labels (discrete, nominal) by constructing a model based on training data to use for classifying new data → [[Decision Boundary]].

[[Class Imbalance]]

## General Process

1. Model construction:

- training set with class labels
- classification rules, decision trees, formulae

2. Model usage:

- Estimate [[Accuracy]]
  - Test set (independent of training set) to compare with results from model
  - Accuracy Rate → [[True positive rate|hit rate]]
- if acceptable use model to classify new [[Dataset|data]]

## Methods

- [[Bayesian Classifier]]
- [[Naive Bayes Classifier]]
- [[Decision Tree]]
- [[Random Forest]]
- [[Logistic Regression]]
- [[Perceptron]]
- [[Adaptive Linear Unit|Adaline]]
- [[Support Vector Machine|SVM]]
- [[K-Nearest Neighbors]]

### Perceptron & Adaline

- Both are not able to converge for data that is not linearly seperable

### SVM vs. Logistic Regression

- Logistic Regression is more prone to [[Outlier|Outliers]]. SVM only look at the support vectors so it isnt as sensitive.
- Logistic Regression can be updated easier with streamed data

also see [[Performance Evaluation Metrics]]