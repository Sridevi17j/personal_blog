---
layout: default
title: Feature Scaling - R Implementation
parent: Data Pre-processing
nav_order: 11
---
The interesting R implementation for Normalization and Standardization is here now.   
Here we check whether we need to go for Normalization or Standardization, for which we take one variable and go for histogram and check whether that variable is skewed or normally distributed.  see below  
### Normality Check
Checked for price and Distance
![](/assets/images/DP/feature-scaling-R/p1.png) 
![](/assets/images/DP/feature-scaling-R/p2.png) 
After Executing above , we know that variables are skewed,
Standardization is not possible. So we opt for Normalization.
### Dataset before Normalization
![](/assets/images/DP/feature-scaling-R/p3.png) 
### Code Executed for Normalization
![](/assets/images/DP/feature-scaling-R/p4.png)
### Dataset after Normalization
![](/assets/images/DP/feature-scaling-R/p5.png)

### Standardization code
![](/assets/images/DP/feature-scaling-R/p6.png)
### Dataset After Standardization
![](/assets/images/DP/feature-scaling-R/p7.png)

Here we end up with Feature Scaling, and we will head up with sampling Techniques in next page. 