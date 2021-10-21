## Overview of the Project
In this project, different supervised machine learning (ML) algorithms are used on [credit loan dataset](https://github.com/elp192/Predict-Credit-Risk/blob/cb4fdaffb7d1a5eed61fe54e349257091e55a2d8/Resources/LoanStats_2019Q1.csv.zip) to predict credit risk. The performance of ML algorithms are compared using the following tools:<br>
- Language: Python - code is written in Jupyter Notebook.
- Libraries: Scikit-learn, Imbalanced-learn

Different techniques are adopted as follows:<br>
1. **Logistic Regression**:
As this problem is an unbalanced classification problem (i.e., bad loans less than good loans), resampling methods need to be used to resample training data. Algorithms are applied for resampling as:<br>
- "*RandomOverSampling*" and "*SMOTE*" algorithms are used for oversampling.<br>
- "*ClusterCentroids*" algorithm is used for undersampling.<br>
- "*SMOTEENN*" algorithm is used for over-and under-sampling.<br>

2. **Ensemble Classifiers**
The following ensemble classifiers are compared:
- "*BalancedRandomForestClassifier*"
- "*EasyEnsembleClassifier*"

The following steps are performed for each technique:

- Applying basic cleaning to the data.
- Splitting data into train and test dataset.
- Training data using the logistic regression and ensemble classifiers (in logistic regression model, resampling algorithm is applied).
- Testing data.
- Calculating balanced accuracy score.
- Calculating confusion matrix.
- Generating classification report.

## Results
**Logistic Regression**
- Random Oversampling<br>

<p img align="center" width="100%">
<img width="500" alt="random_oversampling" src="https://user-images.githubusercontent.com/85843401/138348986-e6fbf7f9-8d9a-4f2b-8715-e1731162d3ea.png">
<figcaption>Figure 1: Balanced accuracy score, confusion matrix, and classification report related to random oversampling algorithm.</figcaption></figure/> 
<p align="center">
</p>

- SMOTE Oversampling<br>

<p img align="center" width="100%">
<img width="500" alt="smote_oversampling" src="https://user-images.githubusercontent.com/85843401/138349002-884b574e-8de3-4b8b-9192-3702daffe2f7.png">
<figcaption>Figure 2: Balanced accuracy score, confusion matrix, and classification report related to SMOTE oversampling algorithm.</figcaption></figure/> 
<p align="center">
</p>

- Cluster Centroids Undersampling<br>

<p img align="center" width="100%">
<img width="500" alt="undersampling" src="https://user-images.githubusercontent.com/85843401/138349008-328e59f4-c648-4dae-87b7-ecbb2af3dbfa.png">
<figcaption>Figure 3: Balanced accuracy score, confusion matrix, and classification report related to cluster centroids undersampling algorithm.</figcaption></figure/> 
<p align="center">
</p>


- Combination of Over- and Under- sampling<br>

<p img align="center" width="100%">
<img width="500" alt="combination" src="https://user-images.githubusercontent.com/85843401/138349021-4c6d20a2-26ab-48c3-a721-99a4d9b789b8.png">
<figcaption>Figure 4: Balanced accuracy score, confusion matrix, and classification report related to combination of over- and under- sampling algorithm.</figcaption></figure/> 
<p align="center">
</p>

**Ensemble Classifiers**
- Balanced Random Forest<br>

<p img align="center" width="100%">
<img width="500" alt="balanced_randomforesr" src="https://user-images.githubusercontent.com/85843401/138349271-9215528f-b6bd-47ab-8aa8-7c508d8f9826.png">
<figcaption>Figure 5: Balanced accuracy score, confusion matrix, and classification report related to balanced random forest algorithm.</figcaption></figure/> 
<p align="center">
</p>

- Easy Ensemble AdaBooster<br>

<p img align="center" width="100%">
<img width="500" alt="easy_ensemble" src="https://user-images.githubusercontent.com/85843401/138349283-3c3aeb67-6c74-42c0-878e-07461c06ce0f.png">
<figcaption>Figure 6: Balanced accuracy score, confusion matrix, and classification report related to easy ensemble AdaBooster algorithm.</figcaption></figure/> 
<p align="center">
</p>

## Summary

