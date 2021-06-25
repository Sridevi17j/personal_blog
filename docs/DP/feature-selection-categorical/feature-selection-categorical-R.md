---
layout: default
title: Feature Selection Categorical Values - R
parent: Data Pre-processing
nav_order: 8
---

Let us get through Feature Selection for Categorical Variables in R. And Yes! the method is - Chi Square Test of Independence.  See the below commands.  
![](/assets/images/DP/feature-selection-categorical-R/p1.png)
Factor index will have true if that variable is categorical variable. See below.  
![](/assets/images/DP/feature-selection-categorical-R/p2.png)
Now see the factor data as well!  
![](/assets/images/DP/feature-selection-categorical-R/p3.png)
See below loop which converts categorical values to labels which is easy to understand.    
![](/assets/images/DP/feature-selection-categorical-R/p4.png)
Below is the dataset before execution of the loop  
![](/assets/images/DP/feature-selection-categorical-R/p5.png)
Below is the dataset after loop execution  
![](/assets/images/DP/feature-selection-categorical-R/p6.png)  

## Chi Square Calculation
We have 21 rows in factor_index, ( Number of columns for categorical values)  
NROW(factor_index) // shows the number of rows for a vector.. Here factor_index is a vector..  
Now we need to iterate 21 variables with target variable "Type".. Loop below...   
![](/assets/images/DP/feature-selection-categorical-R/p7.png)  
And the output is below..
![](/assets/images/DP/feature-selection-categorical-R/p8.png) 
We have to interpret the output like below.  
- if p value is less than 0.05 than we have to reject null hypothesis. (Refer Statistics part3 - Hypothesis Testing). 
- In below picture, first value of p is 2.2e-16  which is equal to -10.01 which is less than 0.05 then we reject NULL Hypothesis.  
We have decided below  
NULL Hypothesis - Two variables are Independent 
Alte Hypothesis - Two variables are dependent.  
So the variable " Suburb" and "Type" are dependent on each other. So we take "Suburb" into consideration.
Note :- 
Variables should adhere the below conditions before go into ML Model.
- Independent variables should be negatively correlated with other Independent variables. 
- Independent variables should be positively correlated with dependent variables. 
After we find out the variable lists, we delete other variables from the dataset and create a subset of dataset to be fed into the further process.
- By Analysing the Chi Square results, address has p value greater than 0.05, so we have to accept the Null Hypo, which is "Address" and "Type" are Independent. Type is the target variable for which the address is not related. So we can ignore Address varible.
- In Correlation Analysis we found below variables to ignore.. 
- Bedroom2  
- Bathroom
- Building Area   
## Create Subset by deleting the variables 
![](/assets/images/DP/feature-selection-categorical-R/p9.png) 

This is how we do Data Preprocessing. And we still behind with Feature Scaling and Sampling Techniques.!!! Will post soon the next!

