## Overview of the Project
In this project, different supervised machine learning (ML) algorithms are used on [credit loan dataset](https://github.com/elp192/Predict-Credit-Risk/blob/cb4fdaffb7d1a5eed61fe54e349257091e55a2d8/Resources/LoanStats_2019Q1.csv.zip) to predict credit risk. The performance of ML algorithms are compared using the following tools:<br>
- Language: Python - code is written in Jupyter Notebook.
- Libraries: Scikit-learn, Imbalanced-learn

Different techniques are adopted as follows:<br>
1. **Logistic Regression**:
As this problem is an unbalanced classification problem (i.e., bad loans less than good loans), resampling methods need to be used to resample training data. Algorithms are applied for resampling as:<br>
- "*Random Oversampling*" and "*Synthetic Minority Oversampling Technique (SMOTE)*" approaches are used for oversampling.<br> In the former, to balance the instances of classes, training set is increased by adding instances which are randomly selected from instances of minority class. In the latter, the instances of minority class is increased; however, instances are created by interpolation. In this approach, closest neighbors to instance of minority class is selected and according their values, new instances are created.
- "*Cluster Centroids*" algorithm is used for undersampling.<br> In undersampling approaches, the number of instances in the majority class is declined. In  *Cluster Centroids* technique, the syntatic data (centroids) representing the clusters is generated using majority class clusters. Then, the size of majority class is decreased by undersampling to be equal to the minority class.<br>
- "*SMOTEENN*" algorithm which is combination of "*SMOTE*" and "*Edited Nearest Neighbors* (ENN)" methods is used.<br> In this approach, firstly, the minority class is oversampled. Next, the data is cleaned using "*SMOTE*".

2. **Ensemble Classifiers**
The following ensemble classifiers are compared:
- "*Balanced Random Forest Classifier*"
- "*Easy Ensemble Classifier*"

## Results
### Logistic Regression<br>
**Random Oversampling**<br>

<p img align="center" width="100%">
<img width="400" alt="random_oversampling" src="https://user-images.githubusercontent.com/85843401/138464624-919f7c75-83eb-4192-bdf2-d8f4ca2d0ec0.png"><figcaption>Figure 1: Balanced accuracy score, confusion matrix, and classification report related to random oversampling algorithm.</figcaption></figure/> 
<p align="center">
</p>

- Balanced accuracy is about 64%.<br>
- For the high risk, precision and recall (sensitivity) is  1% and 62%, respectively.<br>
- For the low risk, precision and recall is about 100% and 65%, respectively.<br>

**SMOTE Oversampling**<br>

<p img align="center" width="100%">
<img width="400" alt="smote_oversampling" src="https://user-images.githubusercontent.com/85843401/138466070-9cf965d9-63aa-4ecf-b676-a3edda533a1f.png">
<figcaption>Figure 2: Balanced accuracy score, confusion matrix, and classification report related to SMOTE oversampling algorithm.</figcaption></figure/> 
<p align="center">
</p>

**Cluster Centroids Undersampling**<br>

<p img align="center" width="100%">
<img width="400" alt="undersampling" src="https://user-images.githubusercontent.com/85843401/138466417-897bbd93-a5b2-4278-a404-4adc0b277071.png">
<figcaption>Figure 3: Balanced accuracy score, confusion matrix, and classification report related to cluster centroids undersampling algorithm.</figcaption></figure/> 
<p align="center">
</p>

**Combination of Over- and Under- sampling**<br>

<p img align="center" width="100%">
<img width="400" alt="combination" src="https://user-images.githubusercontent.com/85843401/138466475-e794af81-70d1-4988-a498-1193d0487c0d.png">
<figcaption>Figure 4: Balanced accuracy score, confusion matrix, and classification report related to combination of over- and under- sampling algorithm.</figcaption></figure/> 
<p align="center">
</p>

### Ensemble Classifiers<br>
 **Balanced Random Forest**<br>

<p img align="center" width="100%">
<img width="400" alt="balanced_random_forest" src="https://user-images.githubusercontent.com/85843401/138467620-30aaa50a-7dd4-4e37-8460-78eaad36f43c.png">
<figcaption>Figure 5: Balanced accuracy score, confusion matrix, and classification report related to balanced random forest algorithm.</figcaption></figure/> 
<p align="center">
</p>

**Easy Ensemble AdaBooster**<br>

<p img align="center" width="100%">
<img width="400" alt="easy_ensemble" src="https://user-images.githubusercontent.com/85843401/138467661-6e4e2155-25a0-4550-8278-4962e517fa1b.png">
<figcaption>Figure 6: Balanced accuracy score, confusion matrix, and classification report related to easy ensemble AdaBooster algorithm.</figcaption></figure/> 
<p align="center">
</p>

## Summary

