# Credit_Risk_Analysis
Data preparation, Statistical reasoning, Machine Learning 

# Overview of the analysis
Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company. Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, we need to employ different techniques to train and evaluate models with unbalanced classes, such as oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, use a combinatorial approach of over and undersampling using the SMOTEENN algorithm. Next, compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Once the analysis are performed, evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

# Results
## Oversample algorithms:
- Naive RandomOverSampler Result

![Screen Shot 2022-09-25 at 9 13 12 PM](https://user-images.githubusercontent.com/65901034/192175560-71733975-7485-4e03-8367-201d745e399f.png)

- SMOTE Oversampler Result

![Screen Shot 2022-09-25 at 9 14 46 PM](https://user-images.githubusercontent.com/65901034/192175650-ba0d261a-019e-4084-886a-0c54177db159.png)

## Undersample 
- ClusterCentroids result

![Screen Shot 2022-09-25 at 9 16 18 PM](https://user-images.githubusercontent.com/65901034/192175740-652e6456-5d95-4024-9616-35a27a4522bd.png)

## Combination (Over and Under) Sampling
- SMOTEENN algorithm

![Screen Shot 2022-09-25 at 9 31 43 PM](https://user-images.githubusercontent.com/65901034/192176909-727d5d59-c60c-49bc-9e3b-7c3f2c5ec9ef.png)

## Ensemble Learners Algorithms:
- Balanced Random Forest Classifier

![Screen Shot 2022-09-25 at 9 33 48 PM](https://user-images.githubusercontent.com/65901034/192177051-37cacd90-1922-4e85-a766-415870b3ebb8.png)

- Easy Ensemble AdaBoost Classifier

![Screen Shot 2022-09-25 at 9 34 07 PM](https://user-images.githubusercontent.com/65901034/192177074-9940d928-15ae-43e0-b581-135085b33bb5.png)



# Summary 
All the models used to perform the credit risk analysis show weak precision in determining if a credit risk is high.
The Ensemble models brought a lot more improvment specially on the sensitivity of the high risk credits. While Adaboost algorithm shows a recall(sensitivity) of 92% so it detects almost all high risk credit, and BalancedRandomForest algorithm did not show any significant improvement (with significance 70%) from linear regression with oversampliong or downsampler or both. On another hand, all models with a low precision to detetct high risk loan, therefore a lot of low risk credits will still be falsely detected as high risk which would penalize the bank's credit strategy. For those reasons, these models are not sufficient to predict credit risk for commericial application.

# Resources
-Data: LoanStats_2019Q1.csv from LendingClub
-Software and tools: jupyter notebook; pandas, numpy, scikit-learn, imbalanced-learn libraries 
