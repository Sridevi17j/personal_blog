---
layout: default
title: Feature Selection Categorical Values - Introduction
parent: Data Pre-processing
nav_order: 7
---

In Previous post, we crossed through feature selection for numerical values, In this post, we are going to see about feature selection for categorical values. And yes! the method is " Chi Square Test of Independence"..   

## Chi Square - Formula
![](/assets/images/DP/feature-selection-categorical-introduction/p1.png)
## Degrees of freedom formula
(number of rows-1)(number of columns-1)
## Chi Square - Explanation
- Let us consider Null Hypo and Alternate hypo, 
- Null Hypo - Two Variables are Independent
- Alternate Hypo - Two Variables are not Independent
- Now calculate degrees of freedom and chi square Test of Independence.
- Calculate critical value with confidence interval.
- If Chi Square Test result is greater than Critical Value, then reject null hypothesis.   
  Note - Use Contigency table for better representation.  
  
## Example in detail
Below is the Contigency Table  
![](/assets/images/DP/feature-selection-categorical-introduction/p2.png)

And we need to calculate rowsum and columnsum like below
![](/assets/images/DP/feature-selection-categorical-introduction/p3.png)
![](/assets/images/DP/feature-selection-categorical-introduction/p4.png)

And we need to calculate Expected Value like below  
EXPECTED VALUE = (ROWSUM*COLUMNSUM)/TOTALSUM   
![](/assets/images/DP/feature-selection-categorical-introduction/p5.png)  
![](/assets/images/DP/feature-selection-categorical-introduction/p6.png)  
![](/assets/images/DP/feature-selection-categorical-introduction/p7.png)  

And we need to calculate the Chi Square value. Please see below 
![](/assets/images/DP/feature-selection-categorical-introduction/p8.png)  
![](/assets/images/DP/feature-selection-categorical-introduction/p9.png)  
![](/assets/images/DP/feature-selection-categorical-introduction/p10.png)  

And finally the sum is below  
![](/assets/images/DP/feature-selection-categorical-introduction/p11.png) 



How to calculate critical value with Degrees of freedom.. Explained below..   
See the table, and here our degrees of freedom is 6 and Confidence Interval is 95% that is 0.95.. See the picture below and we obtain critical value.    
![](/assets/images/DP/feature-selection-categorical-introduction/p12.png)

The Final calculation is explained below.
![](/assets/images/DP/feature-selection-categorical-introduction/p13.png)


Take some rest and come back for next page, such an interesting field,.. Loving this...
