---
title: Python- Part 5
date: "2020-08-30T22:12:03.284Z"
---

Here we go with next...Working with the mtcars dataset which we loaded before.  
### Selecting rows with condition
dst_n1 = dst.ix[(dst['cyl'] == 6) | (dst['mpg'] == 21)]  
### Output
### Creating a new variable
import numpy as np    
dst['NwVar'] = np.log2(dst['cyl])  
### Output
### Adding rows of data frame
import pandas as pd
df1 = pd.DataFrame({'a' : [1,2,3,4], 'b' : [4,5,6,7]})   
df2 = pd.DataFrame({'a' : [7,8,9,2], 'b' : [3,7,8,9]})   
df3 = df1.append(df2)  
### Output
### Adding Columns
df3 = pd.concat([df1.reset_index(drop=True), df2], axis=1) 
### Convert Variables
dst['mpg'] = dst['mpg'].astype(object)    
### Output
### Convert Entire Dataframe
dst = dst.astype(object)  
### Convert numeric to categorical/binning
dst['mpgcat'] = np.where(dst['mpg'] > 20, 'Low', 0)   
### Sorting - ascending order
dst = dst.sort_values('cyl', ascending = True)  
### Output
### Sorting - descending order
dst = dst.sort_values('cyl', ascending = False)  
### Output
### Merge Dataframes
dfrm1 = pd.Dataframe({'id' : [1,2,3], 'Name' : ['Abi', 'Aki', 'Anu' ]})  
dfrm2 = pd.DataFrame({'Age' : [23, 24, 25], 'Income' : [20k, 30k, 40k]})  
### Output
### Joins
dfrm_lftjn = dfrm1.merge(dfrm2, on = 'id', how = 'left')  
dfrm_rhtjn = dfrm1.merge(dfrm2, on = 'id', how = 'right') 
### Output
### Replace values in a variable
a = ("Everything will be alright")  
a.replace("will", "will defientely")  
### Output
