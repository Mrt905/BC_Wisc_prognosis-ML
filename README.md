Breast cancer prognosis prediction using ML approach



Dataset: 

https://archive.ics.uci.edu/dataset/16/breast+cancer+wisconsin+prognostic





Models: 

K-nearest neighbor and Gaussian process classifier

Unsupervised visualization: K-means + Kernel PCA for visualization



The evaluation was performed using 10 runs of nested cross-validation with different random permutations of the dataset, ensuring robust performance estimates.



KNN and GPC achieved similar performance across runs, with mean accuracies of approximately 74.6% and 75.7%, respectively. A Wilcoxon signed-rank test indicated that the difference between the models was not statistically significant (p > 0.05).



For unsupervised learning, K-Means clustering achieved an accuracy of approximately 59.6% after optimal label matching. As expected, this is lower than supervised approaches, since clustering does not use class labels during training.



Overall, the results suggest that both supervised models capture similar structures in the data, while unsupervised clustering provides only limited separation of the classes.

