# Credit_Risk_Analysis
## Overview
Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, I oversampled the data using the RandomOverSampler and SMOTE algorithms, and undersampled the data using the ClusterCentroids algorithm. Then, I used a combinatorial approach of over and undersampling using the SMOTEENN algorithm. Next, I compared two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Once finished, I evaluated the performance of these models and below is my analysis. 

## Results

## Naive Random Oversampling
The recall score for high risk loans is 70%, meaning that most of the loans defined as high risk were identified, but we may have missed identifying 30% of loans as high risk, which means they were false negatives. On the other hand, 63% of low risk loans were low risk, but we may have missed identifying 37% of loans as low risk, meaning 37% were false negative for low risk.

The precision of high risk loans was only 1%. This indicates that we may have incorrectly identified 99% of high risk loans as high risk, they may be false positives. On the other hand, the low risk loan precision was 100%, meaning that these low risk loans were correctly identified as low risk, leaving little to no chance of a loan being incorrectly identified.

Total balanced accuracy score for Naive Random OverSampling algorithm is 67%.

![image](https://user-images.githubusercontent.com/85076259/136495297-3fb6ad27-9c8e-409a-a694-cd3823fdacfb.png)

## Smote Oversampling
The recall score for high risk loans is 63%, meaning that most of the loans defined as high risk were identified, but we may have missed identifying 37% of loans as high risk, which means there were false negative. On the other hand, 69% of low risk loans were low risk, but we may have missed identifying 31% of loans as low risk.

The precision of high risk loans was only 1%. This indicates that we may have incorrectly identified 99% of high risk loans as high risk,which means they may be false positives. On the other hand, the low risk loan precision was nearly 100%, meaning that these low risk loans were correctly identified as low risk, leaving little to no chance of a loan being incorrectly identified.

Total balanced accuracy score is 66%.

![image](https://user-images.githubusercontent.com/85076259/136496860-2ae00a20-be6f-4176-a48e-eafa7366f09a.png)
## Undersampling
The recall score for high risk loans is 63%, meaning that most of the loans defined as high risk were identified, but we may have missed identifying 37% of loans as high risk, which means there were false negative. On the other hand, 69% of low risk loans were low risk, but we may have missed identifying 31% of loans as low risk.

The precision of high risk loans was only 1%. This indicates that we may have incorrectly identified 99% of high risk loans as high risk,which means they may be false positives. On the other hand, the low risk loan precision was nearly 100%, meaning that these low risk loans were correctly identified as low risk, leaving little to no chance of a loan being incorrectly identified.

Total balanced accuracy score is 66%.

![image](https://user-images.githubusercontent.com/85076259/136497222-c156c6de-98f3-4e6d-9e30-91223c2c231b.png)
 ## Smoteenn
The recall score for high risk loans is 71%, meaning that most of the loans defined as high risk were identified. On the other hand, 58% of low risk loans were low risk, but we may have missed identifying 42% of loans as low risk.

The precision of high risk loans was only 1%. This indicates that we may have incorrectly identified 99% of high risk loans, which means they may be false positives. On the other hand, the low risk loan precision was 100%, meaning that these low risk loans were correctly identified, leaving little to no chance of a loan being incorrectly identified. 

Total balanced accuracy score is 64%.

 ![image](https://user-images.githubusercontent.com/85076259/136498079-305bbb52-cf53-43e2-96d1-da9e479e84c6.png)
## Balanced Random Forest Classifier 
The recall score for high risk loans is 64%, meaning that most of the loans defined as high risk were identified. On the other hand, 89% of low risk loans were low risk and only 11% may have missed identifying low risk loans.

The precision of high risk loans was only 3%. This indicates that we may have incorrectly identified 99% of high risk loans as high risk, as they may be false positives. On the other hand, the low risk loan precision was nearly 100%, meaning that these low risk loans were correctly identified as low risk, leaving little to no chance of a loan being incorrectly identified. 

Total balanced accuracy score is 76%.

![image](https://user-images.githubusercontent.com/85076259/136498341-6084cd6f-c7a0-4346-9f6b-290037c61040.png)

## Easy Ensemble AdaBoost Classifier
The recall score for high risk loans is 92%, meaning that most of the loans defined as high risk were identified. On the other hand, 94% of low risk loans were low risk and only 6% may have missed identifying low risk loans. 

The precision of high risk loans was only 9%. This indicates that we may have incorrectly identified 99% of high risk loans as high risk, as they may be false positives. On the other hand, the low risk loan precision was nearly 100%, meaning that these low risk loans were correctly identified as low risk, leaving little to zero chance of a loan being incorrectly identified.

Total balanced accuracy score for this method is 93%. 

![image](https://user-images.githubusercontent.com/85076259/136498629-c4ebd63f-fa0d-471b-bbfe-3622d573e6c5.png)

## Summary
According to our analysis, Balanced Random Forest Classifier and Easy Ensemble AdaBoost Classifier are effective in identifying predictions of credit risk for the loan status. However, performance of the standard algorithm is not great on imbalanced classification problems.I would recommend using Early EnsembleClassifier for this kind of dataset because of the results of the recall as well the higher percentage of a balance accuracy score. This would show that incorrectly identified credit risk is lower and it would have less impact.
