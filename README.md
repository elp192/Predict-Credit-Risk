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

- Applying basic cleaning to the data.<br>
- Splitting data into train and test data.<br>
- Training using the logistic regression/ensemble classifiers and testing (in logistic regression resampling algorithm is applied to training data).<br>
- Calculating balanced accuracy score.
- Calculating confusion matrix.
- Generating classification report.
