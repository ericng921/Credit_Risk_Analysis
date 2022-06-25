# Credit_Risk_Analysis
## Overview of analysis

We obtained a Supervised Learning (with labeled outcome) dataset from LendingClub about credit card credit information. The data in the dataset are imbalanced classification.

The purpose of the analysis is to employ different techniques to train and evaluate models with unbalanced data and to evaluate the performance of these models and make a recommendation on whether they should be used to predict credit risk. We will apply these techniques to balance out the classifications and improve accuracy score.

There are 6 techniques that we have used which are RandomOverSampler, SMOTE, ClusterCentroids, SMOTEENN, BalancedRandomForestClassifier, and EasyEnsembleClassifier.



## Resources

- Dataset: LendingClub [LoanStats_2019Q1.csv](https://github.com/ericng921/Credit_Risk_Analysis/blob/main/Resources/LoanStats_2019Q1.csv)

- Software: Python 3.10, Conda 4.13, jupyter notebook 6.4.11


## Result

The application contains 68470 low_risk and 347 high_risk "loan status"

We split the data using 75/25 method.



- RandomOverSampler - increase the minority class and add to the training set until the majority and minority classes are balanced.

Accuracy score: 65.38%

The high risk precision rate is 1% and the recall rate is at 68%. F1 score is 2%
The low risk precision rate is 100% and recall rate is 62%. F1 score is 77%





- SMOTE - incresing the sample size of minority class

Accuracy score: 66.5%

The high risk precision rate is 1% and the recall is at 64%. F1 score is 2%
The low risk precision is 100% and recall is 69%. F1 score is 81%


- ClusterCentroids - The algorithm identifies clusters of the majority class, then generates synthetic data points, called centroids, that are representative of the clusters. The majority class is then undersampled down to the size of the minority class.

Accuracy score: 54.42%

The high risk precision rate is 1% and the recall is at 69%. F1 score is 1%
The low risk precision is 100% and recall is 40%. F1 score is 57%.




- SMOTEENN - SMOTEENN first oversample the minority class with SMOTE and then clean the resulting data with an undersampling strategy

Accuracy score: 64.85%

The high risk precision rate is 1% and the recall is at 72%. F1 score is 2%
The low risk precision is 100% and recall is 57%. F1 score is 73%.


- BalancedRandomForestClassifier

Accuracy score: 78.78%

The high risk precision rate is 4% and the recall is at 67%. F1 score is 7%
The low risk precision is 100% and recall is 61%. F1 score is 95%

- EasyEnsembleClassifier.

Accuracy score: 92.54%

The high risk precision rate is 7% and the recall is at 91%. F1 score is 14%
The low risk precision is 100% and recall is 94%. F1 score is 97%



## Summary

After applying 6 different techniques, the EasyEnsembleClassifier produces the best result with accuracy score of 92.54%.

It also provides 91% highest recall rate on high risk and 94% highest recall rate on low risk. Its F1 score of low-risk is the highest among all the techniques as well.

To sum up, the algorithms I would recommend to use is EasyEnsembleClassifier model.


