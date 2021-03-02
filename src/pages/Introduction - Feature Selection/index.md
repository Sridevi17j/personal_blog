---
title: Introduction - Feature Selection
date: "2021-02-10T22:12:03.284Z"
---

Here we see the significant part of Data Preprocessing. It is Feature Selection.  Why so this is?  
It is because, failing in this part will lead to the entire failure,.. Now let us see what it is.  
It is the process, where we automatically or manually select variables/features which contribute in predicting target variable or output. Basically selecting features which go as input of ML Model. Selection of irrelevant variables will retrench the accuracy of the Model.  

##Different methods of feature selection
- Correlation Analysis
- Chi Square Test
  
##Correlation Analysis
- It is applied only on numerical data. 
- It ranges from -1 to 1 and represented by r.
- It tells the relation between two variables, whether it is positively correlated or negatively correlated.  
The formula is 
![](./p1.png)

The purpose of this correlation analysis is to identify redundant variables(variables which are positively correlated or carrying the same information) before it is being fed into the Models. Feeding variables which are similar, will increase the complexity of the Models. 

## Correlation Formula and Calculation
Take two variables and check the correlation. Catch sight of below for detailed calculation.  
## Formula for correlation
![](./p1.png)
![](./p2.png)

Now let us get into the practical execution in Excel to get some better understanding.  
- I have taken two variables mpg and cyl from mtcars dataset.   
- I am going to find correlation between those variables, and check whether those are positively correlated or negatively correlated.  
- I am going to use excel formulas, which will be highlighted in the screenshots below. 
## Correlation - Calculation in Excel
![](./p3.png)
![](./p4.png)
![](./p5.png)
![](./p6.png)
![](./p7.png)
![](./p8.png)
![](./p9.png)
![](./p10.png)
![](./p11.png)
![](./p12.png)
![](./p13.png)

