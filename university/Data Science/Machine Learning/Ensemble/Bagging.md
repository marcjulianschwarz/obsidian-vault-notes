---
uni-module: "KDD"
---
# Bagging

An [[Ensemble Method]].

> [!TIP] Analogy
> Diagnosis based on multiple doctors majority vote.

In each iteration some samples are drawn with replacement from the dataset ([[Bootstap]]), on which a classifier model is trained.

Each [[Classification|classifier]] will predict for a given sample and the so called _bagged_ classifier will count the votes and assign the class with the most votes to the sample.

This method can also be applied to [[Regression]] problems by averaging the predictions from each model.

## Advantages

- often better than single models derived from the whole dataset
- more robust against noise
- improved [[Accuracy]] in prediction
