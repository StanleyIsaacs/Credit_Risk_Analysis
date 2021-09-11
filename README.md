# Credit Risk Analysis

## Overview:
We are tasked with building and then evaluating multiple machine learning models to try and predict credit risk.

### Procedure:
  * Oversample data using RandomOverSampler and SMOTE algorithms
  * Undersample data using ClusterCentroid algorithm
  * Take combinatorial approach of over and under sampling using SMOTEEN algorithm
  * Use BalancedRandomForrestClassifier and EasyEnsembleClassifier as two machine learning models to reduce bias

### Resources:
Python, Anaconda, Conda, Jupyter Notebooks,Data Source-LoanStats_2019Q1.csv

### Results:
  * RandomOversamplerModel:
  
    Balanced accuracy score is 65%.
    The high_risk precision is 1% with 62% sensitivity which makes a F1 of 2%.
    The precision is almost 100% with a sensitivity of 68%.
  * SmoteModel:
 
    Balanced accuracy score is 64%.
    The high_risk precision is 1% with 63% sensitivity which makes a F1 of 2%.
    The precision is almost 100% with a sensitivity of 66%.
  * ClusterCentroids:

    Balanced accuracy score is 52%.
    The high_risk precision is 1% with 63% sensitivity which makes a F1 of 1%.
    There are a high number of false positives and the low_risk sensitivity is only 40%.
    
  * SMOTEENN:
  
    Balanced accuracy score is 62%.
    The high_risk precision is 1% with 68% sensitivity which makes a F1 of 2%.
    There are a high number of false positives and the the low_risk sensitivity is 57%.
    
  * BalancedRandomForestClassifier:
  
    Balanced accuracy score is 79%.
    The high_risk precision is 4% with 67% sensitivity which makes a F1 of 7%.
    There are a lower number of false positives so the low_risk sensitivity is now 91% with 100% presicion.
    
  * EasyEnsembleClassifier:

    Balanced accuracy score is 93%.
    The high_risk precision is 7% with 91% sensitivity which makes a F1 of 14%.
    There are a lower number of false positives and the low_risk sensitivity is now 94% with 100% presicion.
    
  ### Summary:
  
  Each model used to perform the the credit risk analysis show a weak precision in figuring out if a credit risk is high.
  The Ensemble models did improve on the sensitivity of the high risk credits.
  The EasyEnsembleClassifier model is a really good option as it shows a recall of 92% so it detects almost all high risk credit but many low risk credits are      falsely flagged as high which would bring their own set of problems. 
  Because the models used etiher showed weak precision or narrowed the precion while allowing for false results, I wouldn't suggest the bank use these models to predict credit risk.
