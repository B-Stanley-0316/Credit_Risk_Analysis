# Credit Risk Analysis

## Overview
Python was used to build and evaluate six machine learning models to predict credit risk from the LendingClub dataset provided. The six machine learning models used in this project are as follows:
* `RandomOverSampler` to oversample data.
* `SMOTE` to oversample data.
* `ClusterCentroids` to undersample data.
* `SMOTEENN` use to use a combination of over- and undersampling.
* `BalancedRandomForestClassifier` to reduce bias and predict credit risk.
* `EasyEnsembleClassifier` to reduce bias and predict credit risk.

## Results

### Naive Random Oversampling
* `RandomOverSampler` 

![CreditRisk](Resources/CreditRiskCount_Random.png)

  * **Balanced Accuracy**: 0.6515938052705158
  
  ![BalancedAccuracy](Resources/OverSampling_BalancedAccuracy_Random.png)
  
  * **Precision**: 1% (High_Risk) / 100% (Low_Risk)
  * **Recall**: 0.62 (High_Risk) / 0.68 (Low_Risk)

  ![CreditRisk2](Resources/CreditRisk_Random.png)


### SMOTE Oversampling
* `SMOTE`

![CreditRisk](Resources/CreditRiskCount_SMOTE.png)

  * **Balanced Accuracy**: 0.6241876870888075
  
  ![BalancedAccuracy](Resources/OverSampling_BalancedAccuracy_SMOT.png)
  
  * **Precision**: 1% (High_Risk) / 100% (Low_Risk)
  * **Recall**: 0.59 (High_Risk) / 0.66 (Low_Risk)

  ![CreditRisk2](Resources/CreditRisk_SMOTE.png)


### Undersampling
* `ClusterCentroids`

![CreditRisk](Resources/CreditRiskCount_Cluster.png)

  * **Balanced Accuracy**: 0.6241876870888075

  ![BalancedAccuracy](Resources/Undersampling_BalancedAccuracy_ClusterCentroids.png)

  * **Precision**: 1% (High_Risk) / 100% (Low_Risk)
  * **Recall**: 0.60 (High_Risk) / 0.43 (Low_Risk)

  ![CreditRisk2](Resources/CreditRisk_ClusterCentroids.png)
  

### Combination (Over and Under) Sampling
* `SMOTEENN`

![CreditRisk](Resources/CreditRiskCount_SMOTEENN.png)

  * **Balanced Accuracy**: 0.5161072635781654
  
  ![BalancedAccuracy](Resources/OverUnder_BalancedAccuracy_SMOTENN.png)

  * **Precision**: 1% (High_Risk) / 100% (Low_Risk)
  * **Recall**: 0.70 (High_Risk) / 0.58 (Low_Risk)

  ![CreditRisk2](Resources/CreditRisk_SMOTEENN.png)

### Ensemble Learners
* `BalancedRandomForestClassifier`

  * **Balanced Accuracy**: 0.7877672625306695

  ![BalancedAccuracy](Resources/BRFC_BalancedAccuracy.png)

  * **Precision**: 4% (High_Risk) / 100% (Low_Risk)
  * **Recall**: 0.67 (High_Risk) / 0.91 (Low_Risk)

  ![CreditRisk](Resources/CreditRisk_BRFC.png)

* `EasyEnsembleClassifier` 

  * **Balanced Accuracy**: 0.925427358175101

  ![BalancedAccuracy](Resources/EasyEnsemble_BalancedAccuracy.png)

  * **Precision**: 7% (High_Risk) / 100% (Low_Risk)
  * **Recall**: 0.91 (High_Risk) / 0.94 (Low_Risk)

  ![CreditRisk](Resources/CreditRisk_EasyEnsemble.png)


### Summary

Given the results above, it appears that `EasyEnsembleClassifier` yields the best results with a **92.5%** accuracy rate and a **7%** precision rate when predicting "High Risk" candidates and a **100%** precision rate when predicting "Low Risk" candidates. While this model seems like the best option given the recall on High Risk is **91%** and **94%** on Low Risk, having that low **7%** precision rate on High Credit Risks is concerning. One can only assume with such a low rate there, the "Low Credit Risks" may be classified as low risk but are actually high risk. With that note of uncertainty, I would not suggest using this model or any of the other models because they are even less accurate.
