---
layout: default
title: Feature Scaling - Normalization
parent: Data Pre-processing
nav_order: 9
---
Here we move through Feature Scaling/Variable Scaling.
### What is feature scaling?
Feature scaling is a method used to normalize independent variables in the dataset. And this method is for continuos variables. 
### Why Feature Scaling?
Example : We have variables like below in a dataset  
Age : From 30 to 80  
Salary : From 30000 to 100000  
If we use the same variables to be fed into the ML Model, then ML Algorithm tends to consider greater values as higher and smaller values as lower, regardless of unit of the values. To avoid this we go for feature scaling
### How to do Feature Scaling
We do feature scaling on variables to make fit those variables( those are different in units) into particular range. It is done on continuous variable. 
### Methods of Feature Scaling
- Normalization 
- Standardization
### Normalization
Normalization is transforming the values into the range from 0 to 1. And below is the formula..  
![](/assets/images/DP/feature-scaling-normalization/p1.png) 
### Example for Normalization
###Calulate Min Value of Variable cyl
![](/assets/images/DP/feature-scaling-normalization/p2.png) 
### Calculate Max Value of Variable cyl
![](/assets/images/DP/feature-scaling-normalization/p3.png) 
### Calculate Min Value of Variable hp
![](/assets/images/DP/feature-scaling-normalization/p4.png) 
### Calculate Max Value of Variable hp
![](/assets/images/DP/feature-scaling-normalization/p5.png)
### Calculate Normalized Value of Variable Cyl
![](/assets/images/DP/feature-scaling-normalization/p6.png)
### Caluclate Normalized Value of Variable hp
![](/assets/images/DP/feature-scaling-normalization/p7.png)

Here we end for now..   

Will catch up with Standardization in the next post!!!
