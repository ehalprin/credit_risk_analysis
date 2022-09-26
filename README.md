# credit_risk_analysis

## Overview

### Purpose

This project was initiated by Jill at LendingClub, a peer-to-peer lending service. The purpose of the project was to analyze a credit card dataset to see if machine learning could be used to evaluate credit risk. 

### Process

This project was completed in Jupyter Notebook, using Python and the SciKit-Learn and Imbalanced-Learn libraries for machine learning.

## Results

### Naive Random Oversampling

- The balanced accuracy score of the Naive Random Oversampling was 65%
- Naive Random Oversampling had a 100% precision for low-risk credit cards, but only 1% precision for high-risk credit cards.
- Naive Random Oversampling had a 61% recall for high-risk credit cards, and 68% recall for low-risk credit cards.

![Results of Naive Random Oversampling](https://github.com/ehalprin/credit_risk_analysis/blob/main/resources/NaiveRandomOverSampling_Results.png)

### SMOTE Oversampling

- The balanced accuracy score of the SMOTE Oversampling was 62%
- SMOTE Oversampling had a 100% precision for low-risk credit cards, but only 1% precision for high-risk credit cards.
- SMOTE Oversampling had a 61% recall for high-risk credit cards, and 64% recall for low-risk credit cards.

![Results of SMOTE Oversampling](https://github.com/ehalprin/credit_risk_analysis/blob/main/resources/SMOTEOversampling_Results.png)

### Cluster Centroids Undersampling

- The balanced accuracy score of the Cluster Centroids Undersampling was 51%
- Cluster Centroids Undersampling had a 100% precision for low-risk credit cards, but only 1% precision for high-risk credit cards.
- Cluster Centroids Undersampling had a 43% recall for low-risk credit cards, and 60% recall for high-risk credit cards.

![Results of Cluster Centroids Undersampling](https://github.com/ehalprin/credit_risk_analysis/blob/main/resources/ClusterCentroids_Results.png)

### SMOTEENN

- The balanced accuracy score of SMOTEENN was 65%
- SMOTEENN had a 100% precision for low-risk credit cards, but only 1% precision for high-risk credit cards.
- SMOTEENN had a 62% recall for low-risk credit cards, and 69% recall for high-risk credit cards.

![Results of SMOTEENN](https://github.com/ehalprin/credit_risk_analysis/blob/main/resources/SMOTEENN_Results.png)

### Balanced Random Forest Classifier

- The balanced accuracy score of the Balanced Random Forest Classifier was 79%
- Balanced Random Forest Classifier had a 100% precision for low-risk credit cards, but only 4% precision for high-risk credit cards.
- Balanced Random Forest Classifier had a 91% recall for low-risk credit cards, and 67% recall for high-risk credit cards.

![Results of Balanced Random Forest Classifier](https://github.com/ehalprin/credit_risk_analysis/blob/main/resources/BalancedRandomForestClassifier_Results.png)

### Easy Ensemble Classifier

- The balanced accuracy score of the Easy Ensemble Classifier was 93%
- Cluster Centroids Undersampling had a 100% precision for low-risk credit cards, but only 7% preciison for high-risk credit cards.
- Cluster Centroids Undersampling had a 94% recall for low-risk credit cards, and 91% recall for high-risk credit cards.

![Results of Easy Ensemble Classifier](https://github.com/ehalprin/credit_risk_analysis/blob/main/resources/EasyEnsembleClassifier_Results.png)

## Summary

### Overview of Results

Overall, the machine models struggled to achieve any level of precision for high-risk credit cards, likely because there were so many more low-risk credit cards than high-risk credit cards. This means that there were a significant number of false positives identified. However, the models were able to get to a relatively high level of recall, meaning that most of the high-risk credit cards were identified, or that there were not many high-risk credit cards missed by the model.

### Recommendation

I would recommend the easy ensemble classifier model for LendingClub to use, though I would suggest they continue to refine it if possible, by collecting more data, removing unimportant features, and/or using more n_estimators. The Easy Ensemble Classifier had an overall accuracy level of 93%, and was particularly strong in recall, even though it was weak in precision. This model could be relied upon to identify most of the high-risk credit cards, even if there are some false positives as well.
