---
title: Outlier Analysis - R
date: "2021-01-20T22:12:03.284Z"
---

##Convert Strings into factor numeric
for(i in 1:ncol(T1))
  {
  if(class(T1[,i]) =='factor')
    {
    T1[,i] = factor(T1[,i], labels=(1:length(levels(factor(T1[,i])))))
  }
}
![](./p1.png)
The original csv file and the file after changing strings to factor numeric is given below to understand the difference better
![](./p2.png)  ![](./p3.png)

## Outlier Analysis
## Boxplots - Distribution and Outlier Check
## Extracting only numeric variables
numeric_index = sapply(T1, is.numeric)
numeric_data = T1[,numeric_index]
cnames = colnames(numeric_data)
for (i in 1:length(cnames))
{
  assign(paste0("gn",i), ggplot(aes_string(y = (cnames[i]), x = "responded"), data = subset(T1))+
           stat_boxplot(geom = "errorbar", width = 0.5)+geom_boxplot(outlier.colour="red", fill = "grey", outlier.shape=18, outlier.size=1, notch=FALSE) + theme(legend.position="bottom")+labs(y=cnames[i], x="responded")+ggtitle(paste("Box plot of responded for", cnames[i])))
  
}

## Plotting plots together
gridExtra::grid.arrange(gn1,gn5,gn2,ncol=3)
gridExtra::grid.arrange(gn6,gn7,ncol=2)
gridExtra::grid.arrange(gn8,gn9,ncol=2)

## Remove Outliers Using Boxplot
df = marketing_train  
val = marketing_train$previous[marketing_train$previous %in% boxplot.stats(marketing_train$previous)$out]  
marketing_train = marketing_train[which(!marketing_train$previous %in% val),]  

##Loop to remove from all variables
for (i in cnames) {
    print(i)
    val = marketing_train[,i][marketing_train[,i] %in% boxplot.stats(marketing_train[,i] %in% val),]

}

## Replace all outlier with NA
## Create NA on CustAge
for(i in cnames) {
val = marketing_train[,i][marketing_train[,i] %in% boxplot.stats(marketing_train[,i])$out]
print(length(val))
marketing[,i][marketing_train[,i] %in% val] = NA
}

marketing_train = knnimputation(marketing_train, k =3)

