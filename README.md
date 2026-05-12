Breast cancer prognosis prediction using ML approach


Dataset: 
https://archive.ics.uci.edu/dataset/16/breast+cancer+wisconsin+prognostic


Data preprocessing:
The missing feature values were replaced using mean imputation and target labels encoded numerically using LabelEncoder. Features were standardized using StandardScaler to ensure zero mean and unit variance.


Models: 
Supervised learning: K-nearest neighbor and Gaussian process classifier
Unsupervised visualization: K-means + Kernel PCA for visualization


Methodology:
Hyperparameters
KNN: k (1,3,5,7,9,11,15,21), metric (euclidean, manhattan)
GPC: kernel (RBF, Matern, RationalQuadratic, DotProduct)
K-means: number of clusters k selected using Elbow method and Sillhouette score


Evaluation:
The evaluation was performed using 10 runs of nested cross-validation (Inner CV: 5-fold StratifiedKFold inside GridSearchCV to select best hyperparameters; outer CV: 5-fold StratifiedKFold generalisation accuracy estimates) with different random permutations of the dataset to ensure robust performance estimates. Balanced accuracy was used as the scoring metric.


Optimal Hyperparameters:
KNN: optimal k values across the 10 runs is shown in the boxplot. Euclidean was consistenly optimal metric across all 10 runs.
GPC: DotProduct was the consistently winning kernel across all 10 runs.
K-means: k = 2 was determined using two methods: Elbow method and Sillhouette score


GPC achieved better performance across runs, with mean accuracy of approximately 79% (KNN mean accuracy approximately 71%). A Wilcoxon signed-rank test and McNemar indicated that the difference between the models was statistically significant (p < 0.05). Randomness affects the conclusion in individual runs, however overall conclusion is that GPC is superior.
KNN accuracy of 59.6% was computed.



