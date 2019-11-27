---
title: Statistics Advanced Part 2
date: "2019-10-16T22:12:03.284Z"
---

If you are able to recollect below topics by your own, it means we are good to go with advanced topics.
- Introduction
- Different areas of statistics
- Jargons used in statistics
- Central Tendency
- Correlation
- CoVariance
- Collinearity
 We will be applying all these in Predictive Analysis.

## Statistics Advanced -Part2
We are going to see below topics in statistics Advanced
- Hypothesis Testing
- ANOVA
- Chi-Square Test

Above are Statistics Techniques that we apply on data to understand the data flow, to understand the data better, and to understand the different types of variable.

## Hypothesis Testing
Hypothesis is nothing but guess or Assumption. When we get a dataset, we will develop some assumption or guess on the data. A statistical hypothesis is an assumption about the population parameter. There are two types Of statistical hypothesis.
- Null hypothesis
- Alternate hypothesis
Null Hypothesis is denoted by H0.
Alternate Hypothesis is denoted by H1.
Whenever we develop the assumption on the data, we need to validate whether the assumption is true or not. Here we validate with statistical Technique, to identify H0 or H1, which is true.
Lets take an example of Car Breakdown.
H0- No petrol
H1- Technical Issue
Here Statistical Technique woule be taking to Mechanic, and identify which one is true.
When we do statistical Technique analysis we get P value.
If p is less than 0.05 then H1 is true.(Alternate Hypothesis is true)
If p is higher than 0.05 then H0 is true.(Null Hypothesis is true)

## Different Statistical Technique
- Correlation Analysis 
- ANOVA
- Chi Square Test

## Correlaion Analysis
In Previous Notes we saw about Correlation Analysis.  It is used to check dependencies between two numeric variable. Since we saw enough about correlation Analysis we will see ANOVA and Chi-Square in Detail. 

## ANOVA
In ANOVA, we use one categorical variable and one Numerical Variable.
ANOVA = Analysis of Variance

Example
We have a categorical variable which has values Poor, Rich, Medium. We calculate Mean of each variable. Here we go for Hypothesis, below
H0- All the Mean are equal
H1- Means are different

Now apply statistical technique(ANOVA) to identify p value.
If P value is less than 0.05 then H1 is true.
If P value is greater than 0.05 the  H0 is true.
If H0 is true ( All the Mean are Equal), then it means there is no Variance, which means Data carrying same info. This Data can not be fed into Model. This is how we analyse the Data. Lets see another Statistical Technique.

## Chi Square Test
In Chi Square Test we deal with Two Categorical Variable. This test is applied when we have two categorical variable from single population (DataSet).
Example
We have two variables, Gender and Credit card spending.
In Gender we have below values
Male
Female
In Credit card spending we have below values
Low
Medium
High
Now Hypothesis Comes into picture which is below
H0- Gender and CC spending rate are dependent
H1- Gender and CC spending rate are independent
(Just checking whether the Gender is having an impact on CC Spending)
Calculating p and analysing the data further will help us to understand the data better. The reason for calculating dependencies between variables, is when two variables are carrying same info, then sending both to ML model will lead to complexity. To avoid this we are doing all our analysis in previous stages itself.