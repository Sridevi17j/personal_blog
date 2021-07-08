---
layout: default
title: Outlier Analysis - R
parent: Data Pre-processing
nav_order: 4
---

Please find the Outlier Analysis in R, Before we proceed with outlier analysis, let us convert categorical values to numerical values, Since we work on R, which accesses RAM, its good to practice to convert strings to values, as in strings every single letter occupies some memory.
Example   
For Gender variable we have male and female as values. Now let us convert male to 1 and female to 2, which is better than male and female, when comes to memory.  Hope this is now understood. And the code is below..  

##Convert Strings into factor numeric
for(i in 1:ncol(T1))   
  {   
  if(class(T1[,i]) =='factor')   
    {   
    T1[,i] = factor(T1[,i], labels=(1:length(levels(factor(T1[,i])))))   
  }   
}    
![](/assets/images/DP/outlier-analysis-R/p1.png)
The original csv file and the file after changing strings to factor numeric is given below to understand the difference better
![](/assets/images/DP/outlier-analysis-R/p2.png)  
![](/assets/images/DP/outlier-analysis-R/p3.png)

## Outlier Analysis
## Boxplots - Distribution and Outlier Check   
## Extracting only numeric variables  
numeric_index = sapply(T1, is.numeric)   
numeric_data = T1[,numeric_index]   
view(numeric_index)     
view(numeric_data)     
cnames = colnames(numeric_data)    
![](/assets/images/DP/outlier-analysis-R/p4.png)   
![](/assets/images/DP/outlier-analysis-R/p5.png)
![](/assets/images/DP/outlier-analysis-R/p6.png)    
for (i in 1:length(cnames))  
{   
  assign(paste0("gn",i), ggplot(aes_string(y = (cnames[i]), x = "responded"), data = subset(T1))+
           stat_boxplot(geom = "errorbar", width = 0.5)+geom_boxplot(outlier.colour="red", fill = "grey", outlier.shape=18, outlier.size=1, notch=FALSE) + theme(legend.position="bottom")+labs(y=cnames[i], x="responded")+ggtitle(paste("Box plot of responded for", cnames[i])))  
  
}   
![](/assets/images/DP/outlier-analysis-R/p7.png)

** Note **    
If you get an error, could not find function ggplot, please do execute below commands.  
install.packages("ggplot2")  
library("ggplot2")  
After executing above commands, run the code.
## Plotting plots together
gridExtra::grid.arrange(gn1,ncol=1)    
Boxplot will look like below  
![](/assets/images/DP/outlier-analysis-R/p8.png)  

The Next step would be replace all outliers with NA and impute missing value analysis on those NA. see below


With this we will end up this. The Detailed outlier analysis will be updated later. 

Stay Tuned for 
- Feature Selection
- Feature Scaling
- Sampling Techniques
  
After all these, we still have python implementation of all these techniques starts from Missing Value Analysis to Sampling Techniques!!.

sssss!!!! Wait!.. And the real Roller coaster ride starts hereafter. Yes.. Machine Learning!!! Much awaited portion!!!.. stay tuned to learn all these one by one:) 