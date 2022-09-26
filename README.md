# Credit_Risk_Analysis
Data preparation, Statistical reasoning, Machine Learning 

# Overview of the analysis
Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company. Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, we need to employ different techniques to train and evaluate models with unbalanced classes, such as oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, use a combinatorial approach of over and undersampling using the SMOTEENN algorithm. Next, compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Once the analysis are performed, evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

# Results
## Oversamplealgorithms:
- Naive RandomOverSampler Result
![Screen Shot 2022-09-25 at 9 13 12 PM](https://user-images.githubusercontent.com/65901034/192175560-71733975-7485-4e03-8367-201d745e399f.png)

- SMOTE Oversampler Result


# Summary 
All the models used to perform the credit risk analysis show weak precision in determining if a credit risk is high.
The Ensemble models brought a lot more improvment specially on the sensitivity of the high risk credits.
The EasyEnsembleClassifier model shows a recall of 92% so it detects almost all high risk credit. On another hand, with a low precision, a lot of low risk credits are still falsely detected as high risk which would penalize the bank's credit strategy and infer on its revenue by missing those business opportunities.
For those reasons I would not recommend the bank to use any of these models to predict credit risk.
