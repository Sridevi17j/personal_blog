---
title: R Programming- Advanced 1
date: "2020-02-19T22:12:03.284Z"
---

I thought of starting Advanced R, but there are more and more basic R Commands are still need to be covered. So we will go through the entire R Basic commands and will start with R Advanced. I have posted screenshot for every single command so that you will catch up with right syntax. Let us start!

What would be the first command as soon we open R Studio..
Yes!! It is rm(list=ls()) - Removing all objects stored in RAM.
Now set current working Directory using setwd command. Now start working on commands...

### Selecting Rows from Dataset
TempData = mtcars.
View(TempData).
TestData = subset(data, select = c("hp", "drat")).
View(TestData).
### Screenshot for above commands
![](./P1.png)
#### Viewing TempData
![](./P2.png)
#### Viewing TestData( After Extracting two variables)
![](./P3.png)
### Selecting rows with condition
TestData1 = TempData[which(TempData$hp == 110),].
In Above Command, from TempData, we are selecting rows which has hp=110 value. As this is Row level operation we are leaving nothing after comma.
### Screesnhot for which command
![](./P4.png)
### Viewing TestData1
![](./P5.png)

### Command to create Matrix
TestMatrix = matrix(11:19, byrow = T, nrow =3) // This will arrange 11 to 19 by 3 rows. If we set byrow = F, it will arrange by column.
We can also mention number of column as ncol.
### Command And Output Screenshots when byrow = T
![](./P6.png)
![](./P7.png)
### Command And Output Screenshots when byrow = F
![](./P8.png)
![](./P9.png)
### Example for ncol and output
![](./P10.png)
![](./P11.png)
### Transpose Matrix- Command
TestMatrix = matrix(11:19, byrow = T, nrow =3)
View(TestMatrix)
t(TestMatrix) // t for transpose
### Screenshots for Transpose of a matrix
![](./P14.png)
![](./P15.png)
### Few more R commands on Matrix
![](./P16.png)
![](./P17.png)
![](./P18.png)

### Command to create Vector
TestVector = c(11, 15, 18, 19)

Just wanted to explain the differnce between vector and matrix as i just browsed and understood, so that you dont need to waste your time on browsing to understand the same. Vector is a list of numbers and it can be either in row or column, whereas Matrix is an array of numbers with rows and columns.
### Vector Command and Output
![](./P12.png)
![](./P13.png)

Let us finish this page with above commands. There are more basic commands, i will update in my next blog post. 

