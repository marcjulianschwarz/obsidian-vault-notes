# Global Modelling

In Global Modelling we try to build a compressed model of a large set of time series. We hope that the model can be trained once and then used to forecast all of the different timeseries that were used for training. 
This of course is again only possible because of [[Takens Theorem]].

Optimally the model would learn different dependencies between the timeseries to prevent the hidden state to grow indefinitely.

One could also have the idea to use [[Clustering]] methods like [[k-means Clustering]] to cluster different timeseries and then training specific models for each cluster. 
This is not really working for high-dimensional data as clustering uses [[Similarity]] which is useless in such high dimensions. 

With [[Historical Consistent Neural Network|HCNNs]] however the identification of a specific series out of the initial set has to be done inside of the model. $tanh$ neurons use diversity instead of similarity so we do not have this problem here. 