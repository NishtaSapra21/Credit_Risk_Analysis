# Credit Risk Analysis

## Overview

  This analysis uses __imbalanced-learn__ and __scikit-learn__ libraries to build and evaluate models using __RandomOverSampler__ , __SMOTE__ , __ClusterCentroids__ ,   __SMOTEENN__, BalancedRandomForestClassifier__ , and __EasyEnsembleClassifier__ algorithms to predict credit risk.
  
  This analysis uses __”Supervised Machine Laerning”__ to predict credit risk. The basic purpose of supervised learning is to split a dataset  into training and         testing sets. The model uses the training dataset to learn from it. It then uses the testing dataset to assess its performance.

## Results

* __Random Oversampling__

    Here instances of the minority class are randomly selected and added to the training set until the majority and minority classes are balanced.

    Let’s have a look at its performance.
  
    Balanced accuracy score for random oversampling is __0.661432911298613__.

    Now, consider following __confusion matrix__ and __classification report__ images. 
    
    ![cm_os](https://user-images.githubusercontent.com/107717882/195459070-a281cbc2-633c-46d8-9dae-9ffdeb91b3dc.png)
    

    ![OS_report](https://user-images.githubusercontent.com/107717882/195459090-73326a6d-925d-4d27-8fb8-2849ff12afac.png)

    
* __SMOTE Oversampling__

    SMOTE is another oversampling approach to deal with unbalanced datasets. In SMOTE, like random oversampling, the size of the minority is increased. The key             difference between the two lies in how the minority class is increased in size.
  
    Balanced accuracy score for SMOTE oversampling is __0.6581159869962674__.

    Now, consider following __confusion matrix__ and __classification report__ images. 
    
    ![cm_SMOTE](https://user-images.githubusercontent.com/107717882/195459151-62092df5-d29e-4d50-9005-2d2a594b9d96.png)


    ![SMOTE_report](https://user-images.githubusercontent.com/107717882/195459169-e5d9936a-b281-46c5-8e96-4d40b0c28f3d.png)

  
* __Undersampling__

    Cluster centroid undersampling is akin to SMOTE. The algorithm identifies clusters of the majority class, then generates synthetic data points, called centroids,       that are representative of the clusters. The majority class is then undersampled down to the size of the minority class.

    Balanced accuracy score for undersampling is __0.5442661782548694__.

    Now, consider following __confusion matrix__ and __classification report__ images. 
    
    ![cm_us](https://user-images.githubusercontent.com/107717882/195459191-20ab0fcd-631a-4284-91d4-005c8ce79f46.png)


    ![US_report](https://user-images.githubusercontent.com/107717882/195459214-51509943-5b9f-4574-9b84-1a1181d5047d.png)

  
* __Combination (over and under) Sampling – SMOTEENN__

    SMOTEENN combines the SMOTE and Edited Nearest Neighbors (ENN) algorithms. SMOTEENN is a two-step process: Oversample the minority class with SMOTE and clean the       resulting data with an undersampling strategy. If the two nearest neighbors of a data point belong to two different classes, that data point is dropped.

    Balanced accuracy score for SMOTEENN is __0.6710719627856143__.

    Now, consider following __confusion matrix__ and __classification report__ images. 
    
    ![cm_SMOTEENN](https://user-images.githubusercontent.com/107717882/195459253-2793927d-9514-4975-94d1-bbf3266b9379.png)


    ![SMOTEENN_report](https://user-images.githubusercontent.com/107717882/195459284-dfb0773c-7774-4a19-a880-c60346f9d644.png)


* __Balanced Random Forest Classifier__

    A balanced random forest randomly under-samples each boostrap sample to balance it.
      
    Balanced accuracy score for Balanced Random Forest Classifier is __0.7885466545953005__.
  
    Now, consider following __confusion matrix__ and __classification report__ images. 
    
    ![cm_BRFC](https://user-images.githubusercontent.com/107717882/195459315-c79a5218-6b3d-4275-ac4e-ec55ab573741.png)


    ![BRFC_report](https://user-images.githubusercontent.com/107717882/195459340-0aeb6c31-eeeb-4456-9f64-afee1a9b88e0.png)
    

* __Easy Ensemble Classifier__

    The classifier is an ensemble of AdaBoost learners trained on different balanced boostrap samples. The balancing is achieved by random under-sampling.
  
    Balanced accuracy score is for Easy Ensemble Classifier is  __0.9316600714093861__.
    
    Now, consider following __confusion matrix__ and __classification report__ images. 
    
    ![cm_eeac](https://user-images.githubusercontent.com/107717882/195459387-265d195d-7ad3-4438-b1d5-033f8606d267.png)

    ![EEAC_report](https://user-images.githubusercontent.com/107717882/195459408-493c52fc-b8e9-4e73-ba16-f6d4d3723ae8.png)

    

## Summary

After analyzing results of each imbalanced and balanced sampling algorithms, it is obvious that the __Easy Ensemble Classifier__ model did the best job to predict credit risk analysis using supervised machine learning as it has highest __recall/sensitivity__  of __0.94__ and highest __f1 score__  of __0.97__ among all models. 

The precision for prediction of the high risk and low risk are not in line with each other. However, the recall (sensitivity) for predicting high risk and low risk are in line. The higher recall is reflected in higher f1 score. 
__Balanced Random Forest Classifier__ has also high recall score __(0.83)__ that makes f1 score high __(0.93)__. 

The __Cluster Centroid Undersampling__ has lowest __recall : 0.40__ and lowest __f1 score : 0.56__.  Also, Random Oversampling, SSMOTE and SMOTEEN have __recall 0.60, 0.69 and 0.57__ respectively with __f1 scores 0.75, 0.81 and 0.72__ respectively. 


Also the average precision for high risk and low risk is same for all algorithms. Here , we don’t have much data of high risk to train our machine. Somehow data unbalancing affects the performance of sampling algorithms. Only, EES gives some satisfactory results but unbalanced distribution of data might raise questions on its high risk credit predictions. 

