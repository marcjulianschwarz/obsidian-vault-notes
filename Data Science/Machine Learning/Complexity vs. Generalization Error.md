# Complexity vs. Generalization Error

Plotting all complexities -> ideal complexity where test loss is minimum
The error is influenced by bias and variance. Bias is the error induced by simpifying the model and variance is the error induced by differing training data.
Both errors oppose each other. Lowering bias will increase variance -> find sweetspot with low bias and low variance.
You can find this minmum with hyperparameter search on the validation set.