---
---

# Train Validation Split


Splitting the [[Dataset]] into a validation and training set -> you can use hyperparameter search on the validation set (not the test set!!!). If the [[Dataset]] is big enough everything is ok, with a small [[Dataset]] however it is difficult to find a good split ration.

A static split might lead to problems where the validation split is not representative (some data is not present in this split). -> [[K-Fold Cross Validation]]