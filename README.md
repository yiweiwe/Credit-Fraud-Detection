# Credit Fraud Detection
## Context
It is important that credit card companies are able to recognize fraudulent credit card transactions so that customers are not charged for items that they did not purchase.

## Content
The datasets contains transactions made by credit cards in September 2013 by european cardholders. This dataset presents transactions that occurred in two days, where we have 492 frauds out of 284,807 transactions. The dataset is highly unbalanced, the positive class (frauds) account for 0.172% of all transactions.

It contains only numerical input variables which are the result of a PCA transformation. Unfortunately, due to confidentiality issues, we cannot provide the original features and more background information about the data. Features V1, V2, ... V28 are the principal components obtained with PCA, the only features which have not been transformed with PCA are 'Time' and 'Amount'. Feature 'Time' contains the seconds elapsed between each transaction and the first transaction in the dataset. The feature 'Amount' is the transaction Amount, this feature can be used for example-dependant cost-senstive learning. Feature 'Class' is the response variable and it takes value 1 in case of fraud and 0 otherwise.

## Inspiration
Identify fraudulent credit card transactions.

## Process and Result
Processed data like normalizing transaction amount variable, and resampled data to get balanced sample dataset

Constructed five logistic regression models by using scikit-learn package according to different C parameter value
after using k-Fold Cross Validation method to resample, got best result on training balanced sample dataset with recall
score 0.95 when C equal to 0.01, got recall score 0.92 on whole test dataset and plotted fancy confusion matrixes

![image](https://user-images.githubusercontent.com/46982385/67971311-f39f6100-fbe2-11e9-8f09-a3d27f20e0d9.png)
![image](https://user-images.githubusercontent.com/46982385/67971342-00bc5000-fbe3-11e9-9324-b31a543b5e15.png)
