# Credit Risk Analysis

## Overview

  This analysis uses __imbalanced-learn__ and __scikit-learn__ libraries to build and evaluate models using __RandomOverSampler__ , __SMOTE__ , __ClusterCentroids__ ,   __SMOTEENN__, BalancedRandomForestClassifier__ , and __EasyEnsembleClassifier__ algorithms to predict credit risk.
  
  This analysis uses __”Supervised Machine Laerning”__ to predict credit risk. The basic purpose of supervised learning is to split a dataset  into training and         testing sets. The model uses the training dataset to learn from it. It then uses the testing dataset to assess its performance.

## Results

* __Random Oversampling__

    Here instances of the minority class are randomly selected and added to the training set until the majority and minority classes are balanced.

    Let’s have a look at its performance.
  
    Balanced accuracy score for random oversampling is __0.661432911298613__.

    Now, consider following __confusion matrix__ and _classification report__ images. 

* __SMOTE Oversampling__

    SMOTE is another oversampling approach to deal with unbalanced datasets. In SMOTE, like random oversampling, the size of the minority is increased. The key             difference between the two lies in how the minority class is increased in size.
  
    Balanced accuracy score for SMOTE oversampling is __0.6581159869962674__.

    Now, consider following __confusion matrix__ and _classification report__ images. 
  
* __Undersampling__

    Cluster centroid undersampling is akin to SMOTE. The algorithm identifies clusters of the majority class, then generates synthetic data points, called centroids,       that are representative of the clusters. The majority class is then undersampled down to the size of the minority class.

    Balanced accuracy score for undersampling is __0.5442661782548694__.

    Now, consider following __confusion matrix__ and _classification report__ images. 
  
* __Combination (over and under) Sampling – SMOTEENN__

    SMOTEENN combines the SMOTE and Edited Nearest Neighbors (ENN) algorithms. SMOTEENN is a two-step process: Oversample the minority class with SMOTE and clean the       resulting data with an undersampling strategy. If the two nearest neighbors of a data point belong to two different classes, that data point is dropped.

    Balanced accuracy score for SMOTEENN is __0.6710719627856143__.

    Now, consider following __confusion matrix__ and _classification report__ images. 

* __Balanced Random Forest Classifier__

    A balanced random forest randomly under-samples each boostrap sample to balance it.
      
    Balanced accuracy score for Balanced Random Forest Classifier is __0.7885466545953005__.
  
    Now, consider following __confusion matrix__ and _classification report__ images. 

* __Easy Ensemble Classifier__

    The classifier is an ensemble of AdaBoost learners trained on different balanced boostrap samples. The balancing is achieved by random under-sampling.
  
    Balanced accuracy score is for Easy Ensemble Classifier is  __0.9316600714093861__.
    
    Now, consider following __confusion matrix__ and _classification report__ images. 

## Summary


