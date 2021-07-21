---
layout: default
title: Decision Tree-Classification-R
parent: Machine Learning - Supervised
nav_order: 4
---

In this post we are going to see, Decision Tree - Regression  
R Implementation.   
rm(list=ls())  
setwd()  
library(rpart)  
library(mass) 
df = birthwt  
View(birthwt)  
Here I am loading birthweight Data for Regression analysis as we are going to  
predict continuous value.  The required library has been uploaded. See below for 
screenshots..
![](/assets/images/ML/DT/REG/p1.png)   
![](/assets/images/ML/DT/REG/p2.png)   

See below for collecting sample and extracting training and test data   

data_index = sample(1:nrow(df), 0.8 * nrow(df))  
View(data_index)  
training_data = df[data_index,]   
View(training_data)   
test_data = df[-data_index,]   
View(test_data)   

See below for screenshots..  

![](/assets/images/ML/DT/REG/p3.png)   
![](/assets/images/ML/DT/REG/p4.png) 
![](/assets/images/ML/DT/REG/p5.png)   

We are going to prepare ML Model. See below.. 

ML_Model = rpart(bwt ~ ., data = training_data, method = "anova")   
View(ML_Model)   

![](/assets/images/ML/DT/REG/p6.png)   
![](/assets/images/ML/DT/REG/p7.png) 

After building Machine Learning Model, We apply the model on the test data.  
test_predictions = predict(ML_Model, test_data[,-10])    

![](/assets/images/ML/DT/REG/p8.png)   

There are different error metrics to measure the error rate. Below are some..  
Mean Squared Error (MSE)  
Root Mean Squared Error (RMSE)   
Mean Absolute Error (MAE)   
Mean absolute percentage error (MAPE)   

Below is the method to calculate   

regr.eval(test_data[,10], test_predictions, stats = c('mae','rmse','mape', 'mse'))   

![](/assets/images/ML/DT/REG/p9.png)

in the above screenshot its calculated. For mape it says 12 % error rate. 
It is mentioned in exponential where we have to convert to %.. 

Hope its clear!..  

Lets move next!!!!





