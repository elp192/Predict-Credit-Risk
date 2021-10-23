## Overview of the Project
In this project, different supervised machine learning (ML) algorithms are used on [credit loan dataset](https://github.com/elp192/Predict-Credit-Risk/blob/cb4fdaffb7d1a5eed61fe54e349257091e55a2d8/Resources/LoanStats_2019Q1.csv.zip) to predict credit risk. The performance of ML algorithms are compared using the following tools:<br>
- Language: Python - code is written in Jupyter Notebook.
- Libraries: Scikit-learn, Imbalanced-learn

Different techniques are adopted as follows:<br>
1. **Logistic Regression**:
As this problem is an unbalanced classification problem (i.e., bad loans less than good loans), resampling methods need to be used to resample training data. Algorithms are applied for resampling as:<br>
- "*Random Oversampling*" and "*Synthetic Minority Oversampling Technique (SMOTE)*" approaches are used for oversampling.<br> In the former, to balance the instances of classes, the training set is increased by adding instances that are randomly selected from instances of minority class. In the latter, the instances of minority class are increased; however, instances are created by interpolation. In this approach, closest neighbors to instance of minority class is selected and according to their values, new instances are created.
- "*Cluster Centroids*" algorithm is used for undersampling.<br> In undersampling approaches, the number of instances in the majority class is declined. In  *Cluster Centroids* technique, the syntatic data (centroids) representing the clusters are generated using majority class clusters. Then, the size of majority class is decreased by undersampling to be equal to the minority class.<br>
- "*SMOTEENN*" algorithm, which is a combination of "*SMOTE*" and "*Edited Nearest Neighbors* (ENN)" methods, is used.<br> In this approach, firstly, the minority class is oversampled. Next, the data is cleaned using "*SMOTE*".

2. **Ensemble Classifiers**
The following ensemble classifiers are compared:
- "*Balanced Random Forest Classifier*"
- "*Easy Ensemble Classifier*"

## Results
In this section, the results of classifiers are presented in Figures 1-6.
### Logistic Regression<br>
**Random Oversampling**<br>

<p img align="center" width="100%">
<img width="450" alt="random_oversampling" src="https://user-images.githubusercontent.com/85843401/138464624-919f7c75-83eb-4192-bdf2-d8f4ca2d0ec0.png"><figcaption>Figure 1: Balanced accuracy score, confusion matrix, and classification report related to random oversampling algorithm.</figcaption></figure/> 
<p align="center">
</p>

- Balanced accuracy is 64%.<br>
- For the high risk, precision and recall (sensitivity) is  1% and 62%, respectively.<br>
- For the low risk, precision and recall are about 100% and 65%, respectively.<br>

**SMOTE Oversampling**<br>

<p img align="center" width="100%">
<img width="450" alt="smote_oversampling" src="https://user-images.githubusercontent.com/85843401/138466070-9cf965d9-63aa-4ecf-b676-a3edda533a1f.png">
<figcaption>Figure 2: Balanced accuracy score, confusion matrix, and classification report related to SMOTE oversampling algorithm.</figcaption></figure/> 
<p align="center">
</p>

- Balanced accuracy is 66%.<br>
- For the high risk, precision and recall (sensitivity) is 1% and 63%, respectively.<br>
- For the low risk, precision and recall are about 100% and 69%, respectively.<br>

**Cluster Centroids Undersampling**<br>

<p img align="center" width="100%">
<img width="450" alt="undersampling" src="https://user-images.githubusercontent.com/85843401/138466417-897bbd93-a5b2-4278-a404-4adc0b277071.png">
<figcaption>Figure 3: Balanced accuracy score, confusion matrix, and classification report related to cluster centroids undersampling algorithm.</figcaption></figure/> 
<p align="center">
</p>

- Balanced accuracy is 54%.<br>
- For the high risk, precision and recall (sensitivity) are 1% and 69%, respectively.<br>
- For the low risk, precision and recall are about 100% and 40%, respectively.<br>


**Combination of Over- and Under- sampling**<br>

<p img align="center" width="100%">
<img width="450" alt="combination" src="https://user-images.githubusercontent.com/85843401/138466475-e794af81-70d1-4988-a498-1193d0487c0d.png">
<figcaption>Figure 4: Balanced accuracy score, confusion matrix, and classification report related to combination of over- and under- sampling algorithm.</figcaption></figure/> 
<p align="center">
</p>

- Balanced accuracy is about 63%.<br>
- For the high risk, precision and recall (sensitivity) are 1% and 68%, respectively.<br>
- For the low risk, precision and recall are about 100% and 58%, respectively.<br>

### Ensemble Classifiers<br>
 **Balanced Random Forest**<br>

<p img align="center" width="100%">
<img width="450" alt="balanced_random_forest" src="https://user-images.githubusercontent.com/85843401/138467620-30aaa50a-7dd4-4e37-8460-78eaad36f43c.png">
<figcaption>Figure 5: Balanced accuracy score, confusion matrix, and classification report related to balanced random forest algorithm.</figcaption></figure/> 
<p align="center">
</p>

- Balanced accuracy is 78%.<br>
- For the high risk, precision and recall (sensitivity) are 3% and 70%, respectively.<br>
- For the low risk, precision and recall are about 100% and 87%, respectively.<br>

**Easy Ensemble AdaBooster**<br>

<p img align="center" width="100%">
<img width="450" alt="easy_ensemble" src="https://user-images.githubusercontent.com/85843401/138467661-6e4e2155-25a0-4550-8278-4962e517fa1b.png">
<figcaption>Figure 6: Balanced accuracy score, confusion matrix, and classification report related to easy ensemble AdaBooster algorithm.</figcaption></figure/> 
<p align="center">
</p>

- Balanced accuracy is about 93%.<br>
- For the high risk, precision and recall (sensitivity) are  9% and 92%, respectively.<br>
- For the low risk, precision and recall are about 100% and 94%, respectively.<br>

## Summary
From the result, conclusions are as follows:<br>
:white_medium_small_square: The balanced accuracy score of regression models is in the range of 54%-66%. However, this value is 78% and 93% for balanced random forest and easy ensemble AdaBooster (ensemble model), respectively.<br>
:white_medium_small_square: In all models, the precision for the high-risk credit is less than 9%. The low precision value means that the number of false positive (FP) is high, and the classifiers are unsuccessful in labeling the credits corectly (i.e., many low-risk credits are considered as high-risk credits). Also, the value of precision for low-risk credits is 100%. This shows the classifiers correctly determine all the low-risk credits.<br>
:white_medium_small_square: In logistic regression models, the recall (sensitivity) is changed between 62%-69% for high-risk credits and 40%-65% for low-risk credits; however, in balanced random forest and easy ensemble AdaBooster (ensemble model), this metrics is 70% and 92% for high-risk credits, respectively and 87% and 94% for low-risk credits, respectively.<br>

Among all the models, the easy ensemble model's accuracy and recall (sensitivity) are higher than other models; however, its precision for high-risk credits is low. This means that there are lots of low-risk credits that are labeled as high-risk credits. So, none of the models is recommended for predicting the credit risk.<br>
