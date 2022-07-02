# Credit Risk Analysis

## Overview
Python was used to build and evaluate six machine learning models to predict credit risk from the LeandingClub dataset provided. The six machine learning models used in this project are as follows:
* RandomOverSampler to oversample data.
* SMOTE to oversample data.
* ClusterCentroids to undersample data.
* SMOTEENN use to use a combination of over- and undersampling.
* BalancedRandomForestClassifier to reduce bias and predict credit risk.
* EasyEnsembleClassifier to reduce bias and predict credit risk.

## Results

### Naive Random Oversampling
* `RandomOverSampler` 
  * **Balanced Accuracy**: 0.6515938052705158
  * **Precision**: 
  * **Recall**: 0.62 (High_Risk) / 0.68 (Low_Risk)

![BalancedAccuracy](Resources/OverSampling_BalancedAccuracy_Random.png)
![CreditRisk](Resources/CreditRiskCount_Random.png)
![CreditRisk2](Resources/CreditRisk_Random.png)

### SMOTE Oversampling
* `SMOTE`
  * **Balanced Accuracy**: 0.6241876870888075
  * **Precision**: 
  * **Recall**: 0.59 (High_Risk) / 0.66 (Low_Risk)

![BalancedAccuracy](Resources/OverSampling_BalancedAccuracy_SMOT.png)
![CreditRisk](Resources/CreditRiskCount_SMOTE.png)
![CreditRisk2](Resources/CreditRisk_SMOTE.png)

### Undersampling
* `ClusterCentroids`
  * **Balanced Accuracy**: 0.6241876870888075
  * **Precision**: 
  * **Recall**: 0.60 (High_Risk) / 0.43 (Low_Risk)

![BalancedAccuracy](Resources/Undersampling_BalancedAccuracy_ClusterCentroids.png)
![CreditRisk](Resources/CreditRiskCount_Cluster.png)
![CreditRisk2](Resources/CreditRisk_ClusterCentroids.png)

### Combination (Over and Under) Sampling
* `SMOTEENN`
  * **Balanced Accuracy**: 0.5161072635781654
  * **Precision**: 
  * **Recall**: 0.70 (High_Risk) / 0.58 (Low_Risk)

![BalancedAccuracy](Resources/OverUnder_BalancedAccuracy_SMOTENN.png)
![CreditRisk](Resources/CreditRiskCount_SMOTEENN.png)
![CreditRisk2](Resources/CreditRisk_SMOTEENN.png)

### Ensemble Learners
* `BalancedRandomForestClassifier`
  * **Balanced Accuracy**: 0.7877672625306695
  * **Precision**: 
  * **Recall**: 0.67 (High_Risk) / 0.91 (Low_Risk)

![BalancedAccuracy](Resources/BRFC_BalancedAccuracy.png)
![CreditRisk](Resources/CreditRisk_BRFC.png)

* `EasyEnsembleClassifier` 
  * **Balanced Accuracy**: 0.925427358175101
  * **Precision**: 
  * **Recall**: 0.91 (High_Risk) / 0.94 (Low_Risk)

![BalancedAccuracy](Resources/EasyEnsemble_BalancedAccuracy.png)
![CreditRisk](Resources/CreditRisk_EasyEnsemble.png)


### Summary
