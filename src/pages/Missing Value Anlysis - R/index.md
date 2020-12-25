---
title: Missing Value Analysis
date: "2020-12-15T22:12:03.284Z"
---

This page is going to be full of R commands on topic Missing Value Analysis. 

##Load Required Libraries
x = c(“ggplot2”, “corrgram”, “DMWR”, “caret”, “randomforest”, “unbalanced”, “C50”, “dummies”, “e1071”, “Information”, “MASS”, “rpart”, “gbm”, “ROSE”)

## Read Data
##Read Data
marketing_train =read.csv(“marketing.csv”,  header = T, na.strings = c(“”,””,”NA”))

##List the column names
names(Marketing_train)

## Explore the data
str(Marketing_train)  

##Create Dataframe with missing percentage
missing_val = data.frame(apply(marketing_train, 2, function(x) {sum(is.na(x))}))
view(missing_val)

##Convert row names into column
Mmssing_val$columns = row.names(missing_val)
Row.names(missing_val) = NULL

##Rename the variable name
names(missing_val)[1] = “missing_percentage”
sum(is.na(marketing_train$custAge))

## Calculate percentage
missing_val$missing_percentage = (missing_val$missing_percentage/nrow(marketing_train)) = 100

#Arrange in descending order
Missing_val = missing_val[order(-missing_val$missing_percentage),]

##Rearranging the columns
missing_val = missing_val[,c(2,1)]

## write the output results back into the disk
write.csv(missing_val, “Missing_perc.csv”,  row.names = F)

##plot bar graph for missing values
Ggplot(data = missing_val[1:3,], aes(x=reorder(columns, -missing_percentage), y = Missing_percentage))+geom_bar(stat = “identity”, fill = grey)+xlab(“Parameter”)+ggtitle(“Missing data percentage (Train)”) + theme_bw()

##Mean Method
marketing_train$custAge[is.na(marketing_train$custAge)] = mean(marketing_train$custAge, na.rm = T)

##Median Method
marketing_train$custAge[is.na(marketing_train$custAge)] = median(marketing_train$custAge, na.rm = T)

##KNN  Imputation
marketing_train = knnImputation(marketing_train, k = 5)
sum(is.na(marketing_train))
