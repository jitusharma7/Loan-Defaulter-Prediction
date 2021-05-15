# Loan-Defaulter-Prediction
The aim of project is to build a higher accurate model and  identify the key factors which are main driving factor for loan Defaulter.

## Table of Content
  * [Overview](#Overview)
  * [Problem_Definition](#Problem_Definition)
  * [Exploratory_Data_Analysis](#Exploratory_Data_Analysis)
  * [Data_Preprocessing](#Data_Preprocessing)
  * [Model_Building](#Model_Building)
  * [Result](#Result)
  * [Business_Recommendation](#Business_Recommendation)
  * [Credit](#Credit)
  
## Overview
 Loan default occurs when a borrower fails to pay back a debt according to the initial arrangement.. The higher loan defaulter rate is shown as failure of bank to identify eligible customer for loan.

**Impact of attrition on Business**
Banks mainly make money from the interest they charge on loans, and when they are unable to collect the owed interest payments from NPLs, it means that they will have less money available to create new loans and pay operating costs. When the percentage of non-performing loans increases, the lender’s stock price will also go down. The NPLs a bank holds in its books, the less attractive it is for potential investors because its future profitability will suffer if the lender will not earn an income from its credit business.
 According to Deloitte, the average cost-per-hire is $4,000. This cost can be vary by country,region,industry,
 
 So loan default  is vital problem  and need to build suitable model and identify what are the key factor which lead to loan default.
 
 
 ## Problem_Definition
 One leading institute  is facing challenges about loan default rate where customer  not paying loan amount as per agreements. 
 
 The institute   is trying to address this problem by identifying patterns in their existing loan defaulteres  using Machine learning algorithms.
 

 
## Exploratory_Data_Analysis
* Among those who have already credit  policy ,shows higher fico value .

  <img src="/fico%20credit%20policy.PNG" width="300">

* Mostly customer log annual income range is from 10 to 13.

 <img src="/log%20income.PNG" width="300">      
      


## Data_Preprocessing
* Encoding the Status column as 1and 0
* Dropping three features 'SLNO','Candidate Ref' and 'Location' dueto high cardinality
* Applying Label Encoding to'offered band' ordinal feature.
* Applying one hot encoding to restof the categorical features
* Used drop_first feature of one hotencoding to avoidmulticollinearity
* Checked for multicollinearity using correlation mapand variance Inflation factor,Two features 'Pecent hike expected in CTC' and'Percent hike offered in CTC' has been removed

    <img src="/VIF.PNG" width="400">


## Model_Building
* XG Boost performs better thanother models
* Hyperparameters tuning isdone by RandomizedSearchCV for xgboost
* It has a higher accuracy of83.24%
* True Negative is almost doublethan false negative
* Rest of the models have verypoor performance in terms ofpredicting true negative values
* True negative values are crucialbecause it is important to knowwho will not join theorganization


     <img src="/ModelComparison.PNG" width="400">

## Result
* XG Boost classifieroutperforms here among all model with 83.24% accuracy
* Feature importance score from XGBoost classifier
* Top 3 important features = 'Percent difference CTC', 'Duration to accept offer', 'Age'
* Least 3 important features = 'Joining Bonus_Yes', 'LOB_EAS', 'LOB_Healthcare'

## Business_Recommendation
* Firm should focus on 3 important features 'Percent difference CTC', 'Duration to accept offer'& 'Age'
* Firm should introduce new offering/schemes  based on these 3 features combination so that attrition rate can reduce.

## Credit
[dare2Compete](https://https://dare2compete.com/) - This project has been done on this competitive platform.
