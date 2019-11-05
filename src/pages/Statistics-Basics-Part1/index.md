---
title: Statistics Basics Part 1
date: "2019-10-14T22:12:03.284Z"
---

# Data Science - Notes 2
In Notes1, we covered Introduction and all basic information. From Notes 2, we actually enter into the course.
Topics to be covered in Notes 2
- Statistics
- Basic Statistics
- Advanced Statistics

## Basic Statistics
Statistics is the science of conducting studies to collect organize and summarize, analyse and draw conclusion out of data. In Simple words apply statistics on Raw Data to get some meaningful information, or in another words, we can say like, change unorganized data into organized Data by the help of statistics techniques. Statistics gives first insights to business, It helps in narrow down the data.

### Types of  Datasets we handle:
Primary Data  - Data limited within organization
Example: Data related to employees working in the organization...
Seondary Data - Data Available in Public
Example: Some weather reports which is available in the internet...

### Uses of this statistics:
Statistics has been used everywhere, below are some example areas..
Healthcare, Education, Business, Insurance, Marketing, Telecom

### Different Areas of Statistics
There are two types
- Descriptive Statistics 
- Inferential Statistics

## Descriptive Statistics:
Its the first level of applying statistics technique on Raw Data to understand the meaning of it. It gives basic representation of entire population. Numerical and Graphical Technique is available in Descriptive statistis.

Numerical Technique:
Key terms of this Numerical Technique are Mean, Mode, Median, Variance, Standard Deviation and Percentage. Using these terms, some better understanding of the data is achieved at the first level.

Graphical:
Key terms used in here are Bar Graph, Scatter Plot, Histogram, Pie chart, Line chart and graphical representation of Data for understand the meaning within
  
## Inferential statistics:
After descriptive analysis (understanding the data), but how you deliver your insights to client. 
Thats where inferential statistics comes into picture. 

### Difference between Desriptive and Inferential Statistics
By explaining the difference between descriptive and inferential, we can have a better understanding! Descriptive statistics uses the data to provide descriptions of the population, either through numerical calculations or graphs or tables. Inferential statistics makes inferences and predictions about a population based on a sample of data taken from the population.

## Advanced Statistics
In Advanced statistics we are going to see below topics.
- Covariance
- Correlation
- Collinearity

### Covariance
If you have two variables x, y, How the two variables are related in a linear way is Covariance. If Covariance is positive then, two variables have positive linear relationship. If Covariance is negative then, two variables have negative linear relationship
Meaning for Linear-(Constant and Variable connected throgh a straight line, in simple way relationship between variables)
       
### Problem with Covariance
When the two variables are in different scale, it is bit complicated to mention the covariance in a right scale.For example, when you draw a connection line between height and distance, height will be in ft and distance will be in km, when you get covariance value 3000, how to identify whether it is positively related or Mediam related? 
To avoid this, we have correlation which is explained below in detail, 

### Correlation
It is a scaled version of covariance. It tells the dependency between two independent variables. correlation varies from -1 to 1. If -1, then two variables are negatively correlated, if +1, then it is positively correlated, if 0 then no correlation.

### Difference between covariance and correlation
#### Covariance
covariance varies from -infinity to +infinity
It provides direction of relationship 
It is dependent on scale of variables
It shows how much two variables vary together

#### Correlation
correlation varies from -1 to 1
It provides direction and strength of relationship
It is independent of scales of variables
It shows how much two variables are strongly connected

### Importance of covariance and correlation
They both help in identifying the dependency between variables. Mainly used in banking and finance sectors. To develop any Model, we need variables, and these two help in identifying the dependency between variables, which helps in reducing variables carrying same or dependent information. 

### Explanation in Detail
To build any Model, we need variables, Say for example if we have ten variables and we send all ten for Model, then Model will become more complex, so to save time, complexity, if we have any redundant variables,or any variables which are highly correlated, then we can remove one, if they two carrying same information.





