---
title: Introduction - Missing Value Analysis
date: "2020-09-30T22:12:03.284Z"
---
We saw indispensable commands of R and Python for DataScience. Ofcourse what we saw is just a Wave and the Ocean to be crossed is still left out. But let us cross wave by wave, which will undoubtedly make us cross the ocean.

In this page we are going to see Data Preprocessing Techniques. Data preprocessing is nothing but preparing the data in proper format for further analysis. Like handling missing values etc. Below are some of the techniques.

- Missing Value Analysis
- Outlier Analysis
- Feature Selection
- Feature Scaling
- Sampling Techniques
  
Lets see few words about every topic and every single topic will be elucidated in a separate post.

### Missing Value Analysis
The Dataset that we have collected for analysis, may or may not have missing values, which means the column in the dataset may or may not have all the values. If the  particular variable/column has missing values more than 35% we need to drop that column itself.If less than 35% please proceed with filling up missing values. 

How do we get Missing Values
- Human Error
- Refuse to answer while filling
- Optional box in Questionnaire

## When to drop the column 
If the particular column has missing values more than 35%
##When to proceed with Analysis 
If the particular column has missing values less than 35%

## Methods to fill Missing Values
1. Central Statistics (Mean,Median,Mode)
2. KNN Imputation
3. Prediction Method(ML)

Calulate missing values using any one of above methods and identify which value is nearest one and follow that method.  
## In the dataset, 
- Take the column in which missing value analysis to be done.  
- Remove one value which already exists, it can be any value from that column.
- Now using above methods(Central statistics, KNN Imputation, Prediction Method (ML)) calculate the value.
- We get one value for each method, now compare with the removed value.
- Which is the nearest matching value, fix that method.
  
## Example
- Take the column where missing value analysis to be done
- For example if we have value 45 in one place, remove that.
- Now use methods to find out the missing value.
- For Example, if we get below values in methods
-  Central Statistics - 40
-  KNN Imputation - 22
-  Prediction Method - 33
-  Then the nearest value is 40, which we got in Central Statistics method. So we can use that method for missing value analysis.  

Now let us see Missing value analysis using R and Python. 
Now Exit and Move up for those topics.!!!




