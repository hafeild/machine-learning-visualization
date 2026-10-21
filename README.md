# Machine learning visualization

This repository contains a self-contained, single page web application for
visualizing machine learning concepts and algorithms. The visualizations are
designed to help understand how different machine learning models work and how
they make predictions.

The page provides several built in datasets but also allows the user to upload their own in CSV, TSV, or Excel formats. Datasets can be saved to local storage or exported.


## Feature visualization and normalization

The currently loaded dataset can be visualized in a scatter plot, with the ability to select which features to plot on the x and y axes. Up to five dimensions can be visualized at once, with the fourth and fifth dimensions represented by color and shape or size, respectively. The user can also apply normalization techniques to the features and see how it affects the data distribution. The following normalization techniques are available:

  - min-max scaling
  - mean scaling
  - standardization (Z-score normalization)
  - unit length normalization

If used in combination with supervised learning, only the training set are used for the normalization parameters.

Features can be binned into discrete categories, with the ability to specify the number of bins and the binning method (equal width or equal frequency). The user can visualize the binned features and see how it affects the data distribution. One-hot encoding is also available for categorical features, allowing the user to convert categorical features into binary features. The user can visualize the one-hot encoded features and see how it affects the data distribution. Reasonable names are automatically generated for the new features, but the user can also specify their own names.

Simple transformations can be applied to the features, including logarithmic, square root, and exponential transformations. The user can visualize the transformed features and see how it affects the data distribution.


## Unsupervised learning

### K-means clustering

The K-means clustering algorithm can be applied to the dataset, allowing the user to specify the number of clusters. The algorithm will iteratively assign data points to clusters based on their proximity to the cluster centroids, and update the centroids until convergence. The user can step through these one at a time, or run it at a fast or slow pace. Up to five dimensions can be visualized at once, and the user can also visualize the cluster centroids and the decision boundaries.

In addition, a "find the right value of k" tool is available, which runs the K-means algorithm for a range of k values and plots k versus the resulting inertia (sum of squared distances to the nearest cluster center), sillouette coefficient, Calinski-Harabaz index, and Davies-Bouldin Index to help determine the optimal number of clusters (four separate plots are generated, one for each metric). In addition, selecting a value of k and one of the aforementioned metrics will show the resulting cluster assignments and visualize how the metric was calculated.

### Hierarchical clustering

The hierarchical clustering algorithm can be applied to the dataset, allowing the user to specify the number of clusters. The algorithm will iteratively merge or split clusters based on their similarity, creating a dendrogram that shows the hierarchy of the clusters. The user can visualize the dendrogram and cut it at a specific level to obtain the desired number of clusters.

### Collaborative filtering

The collaborative filtering algorithm can be applied to the dataset, allowing the user to specify the number of neighbors to consider when making predictions. The algorithm will use the ratings of similar users to predict the ratings for a given user, and can be used for recommendation systems. The user can visualize the predicted ratings and the similarity between users.


## Supervised learning

For supervised learning, a target feature (label or dependent variable) must be selected from the dataset. The user can choose from a variety of supervised learning algorithms, including linear regression, logistic regression, k-nearest neighbors, decision trees, and artificial neural networks. The user can also specify hyperparameters for each algorithm and visualize the resulting model.

An option with all supervised learning algorithms is to split the dataset into a training set and a test set, with the ability to specify the percentage of data to use for training. The user can also choose to shuffle the data before splitting it. A data split created for one of the algorithms should carry over to the other algorithms, so that the same training and test sets are used for all supervised learning algorithms until they are explicitly changed by the user. Cross-validation is also available for all supervised learning algorithms, allowing the user to specify the number of folds to use. The user can visualize the training and test sets, as well as the cross-validation folds.

The visualizations for all supervised learning algorithms should include an animation of the training (when appropriate) that shows the classification of the training data up to that point, as well as the decision boundaries and the predicted labels for the test data. Users have the option of walking through the classification or regression process for each of the testing observations step by step. The user can also visualize the performance metrics for each algorithm based on whether it's regression or classification. Regression includes RMSE, MAE, and R-squared. Classification includes accuracy, precision, recall, F1 score, area under the ROC curve, and confusion matrix.

### Linear regression (regression)

The linear regression algorithm can be applied to the dataset, allowing the user to fit a linear model to the data. The user can visualize the fitted line and the residuals.

### Logistic regression (binary classification)

The logistic regression algorithm can be applied to the dataset, allowing the user to fit a logistic model to the data. The user can visualize the fitted curve and the predicted probabilities. They can also enable ridge or lasso regularization, and specify the regularization strength. The user can visualize the effect of regularization on the model coefficients and the decision boundary.

### k-nearest neighbors (multi-class classification; regression)

The k-nearest neighbors algorithm can be applied to the dataset, allowing the user to specify the number of neighbors to consider when making predictions, the distance metric to use (manhattan, euclidean, etc.), and the voting scheme (majority, weighted, etc.). The user can visualize the nearest neighbors and the resulting predictions in up to five dimensions (with class label or dependent variable being visualized as color or shape). The user can also visualize the decision boundaries and the predicted labels for the test data.

### Decision trees (multi-class classification; regression)

The decision tree algorithm can be applied to the dataset, allowing the user to build a decision tree model. The user can visualize the decision tree and see how it makes decisions based on the input features as well as the pruning process. The user can also visualize the decision boundaries and the predicted labels for the test data. The user can specify the criteria for splitting the nodes (gini impurity, entropy, etc.), the maximum depth of the tree, and the minimum number of samples required to split a node. The user can also visualize the effect of these hyperparameters on the model performance.

### Artificial neural networks (multi-class classification; regression)

The artificial neural network algorithm can be applied to the dataset, allowing the user to build a feedforward neural network model. The user can visualize the architecture of the neural network, including the number of layers and neurons in each layer. The user can also specify the activation functions for each layer, the learning rate, and the number of epochs for training. The user can visualize the training process, including the loss and accuracy over epochs, as well as the decision boundaries and predicted labels for the test data.