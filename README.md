# Supervised Learning: SVM, Decision Tree & AdaBoost - Finding Donors for CharityML

In this project, the performance of the above supervised algorithms are tested to accurately model an individuals' income using the data collected from the 1994 U.S. Census. Then, the best candidate algorithm is chosen from preliminary results and further optimized to best model the data. The goal with this implementation is to construct a model that accurately predicts whether an individual makes more than $50,000. This sort of task can arise in a non-profit setting, where organizations survive on donations. Understanding an individual's income can help a non-profit better understand how large of a donation to request, or whether or not they should reach out to begin with. While it can be difficult to determine an individual's general income bracket directly from public sources, this value can be inferred from other publicly available features.

The dataset for this project originates from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Census+Income). The datset was donated by Ron Kohavi and Barry Becker, after being published in the article "Scaling Up the Accuracy of Naive-Bayes Classifiers: A Decision-Tree Hybrid". You can find the article by Ron Kohavi online. The data we investigate here consists of small changes to the original dataset, such as removing the 'fnlwgt' feature and records with missing or ill-formatted entries.

## Tools Required
The general requirements for this project are as follows:
- numpy
- pandas
- matplotlib
- seaborn
- sci-kit learn
-

## Contents

- **Basic Exploration and Visualization of Data**
- **Data Preprocessing**
  - **Transforming Skewed Continuous** - Features A dataset may sometimes contain at least one feature whose values tend to lie near a single number, but will also have a non-trivial number of vastly larger or smaller values than that single number. Algorithms can be sensitive to such distributions of values and can underperform if the range is not properly normalized.
  - **Normalizing Numerical Features** - In addition to performing transformations on features that are highly skewed, it is often good practice to perform some type of scaling on numerical features. Applying a scaling to the data does not change the shape of each feature's distribution; however, normalization ensures that each feature is treated equally when applying supervised learners. Note that once scaling is applied, observing the data in its raw form will no longer have the same original meaning, as exampled below.
- **Creating a Training and Predicting Pipeline** - To properly evaluate the performance of each model chosen, it's important that we create a training and predicting pipeline that allows us to quickly and effectively train models using various sizes of training data and perform predictions on the testing data.
- **Model Tuning** - Using grid search (GridSearchCV) with different parameter/value combinations, the best performing model is tuned for even better results.
- **Extracting Feature Importance and Feature Selection** - An interesting question here is, how does a model perform if we only use a subset of all the available features in the data? With less features required to train, the expectation is that training and prediction time is much lower — at the cost of performance metrics.
