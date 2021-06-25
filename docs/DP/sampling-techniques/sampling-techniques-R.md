---
layout: default
title: Sampling Techniques - R
parent: Data Pre-processing
nav_order: 13
---
Knowing this would be the next topic, We can directly get in. Here we see three sampling techniques. Below is the first.  
### Simple Random Sampling
In simplified sampling we execute below R code   
Sample_Test_dataset = Test_dataset[sample(nrow(Test_dataset), 1000, replace = F ),]   

Sample_Test_dataset - Sample  
Test_dataset        - Dataset from which we take sample  
sample              - It is a built in function  
nrow()              - First arguement for sample function is the total number of rows of the dataset   
1000                - Number of rows taken for sample  
replace = F         - Rows once taken should not be taken again   

Since this is a row level operation, we end up with comma.. in the code. 
![](/assets/images/DP/sampling-techniques-R/p1.png)  
The original dataset is having 13k rows. See below
![](/assets/images/DP/sampling-techniques-R/p2.png)  

As per above programming the sample should have 1k observations.. see below..
![](/assets/images/DP/sampling-techniques-R/p3.png)

Hope the above one is clear.  The next sampling is below  

### Stratified Sampling
stratas = strata(Test_dataset, c("SellerG"), size = c(60, 100, 100, 100, 50, 60, 1, 1, 1), method = "srswor")
stratas 

