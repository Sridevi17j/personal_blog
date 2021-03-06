---
title: R Part- 1
date: "2020-02-10T22:12:03.284Z"
---

In this page, we are going to see R commands. Try to install R and practice commands in the environment which will be more practical. Before we start it is time to remember below points.
- ctrl+Enter- or Run Button to run the command
- Output for every command will be displayed in console. (Bottom Left)
### R Commands Basics- 2
- rm(list=ls()) //First command to be executed as soon as we open the R Studio to clear R objects from RAM.
#### Listing Objects
- ls() //lists if any objects in RAM
#### Getting and Setting current working directory
- getwd() //getting the current working directory. 
- setwd() //setting the working directory.
#### Example for setwd()
- setwd("C:/Users/Sridevi P/Desktop/Data Science/R Programs")
![](./P1.png)
#### Listing files in the Directory
- list.files() //Lists files in the current directory
- list.files("path") //Lists files in the directory mentioned in path.
- Example:
- list.files("C:/Users/Sridevi P/Desktop/Data Science/R Advanced/")
### Reading and Writing files in R
We saw few commands with preloaded Dataset mtcars. Now we are going to see about Loading external files into R.
#### Loading Text File
TempObj1 = read.delim("Filename.txt", sep = "\t", header = TRUE)
- TempObj  // Temporary object to save the text file.
- read.delim // Function to load the text file
- sep = "\t" // Field separator by space.
- header = TRUE // If this is set to TRUE, then The first row will be treated as row names. We can also make it as FALSE if we dont want the first row to be treated as row names.
#### Screenshot of the command-Loading txt file
![](./P2.png)
#### After Loading, Viewing the content of text file
![](./P3.png)
Actually the text file has below content.
![](./P4.png)
#### Loading CSV File
TempObj3 = read.csv("FileName.csv", header = F) 
- TempObj3 // Temporary object to save the csv file.
- read.xlsx // Function to load csv file
- Header = F // First row will not be treated as row names.
- For Example i have cars.csv file placed in my working directory, which i am loading to TempObj3 and then viewing it. Screenshots below
#### Screenshot of command- Loading CSV File 
![](./P6.png)
#### After Loading, Viewing the content of csv file
![](./P7.png)
#### Writing data to CSV output file
- mc = mtcars // assigning mtcars(preloaded dataset to a object)
- write.csv(mc, "data_output.csv", row.names = T)
- write.csv // It is a function to write into o/p file in csv format.
- data_output.csv // This is the name of output file. This file will be stored in the working directory we set prior using command setwd.
- rownames=T // First row will  be treated as row names as it is set to True.
#### Write CSV to a file- Screenshot
Here we write CSV to a new output file, which will be saved in our working directory. Below screenshot explains the command and see output in console.
![](./P8.png)
#### Loading Xls File
TempObj2 = read.xlsx("Filename.xlsx", sheetIndex = 1, header = TRUE)
- TempObj2 // Temporary object to save the xls file.
- read.xlsx // Function to load xls file
- sheetIndex = 1 // First sheet of the xls file would be read. We need to mention the sheetIndex as we have many sheets in the xls.
- header = TRUE // FIrst row of the data will be treated as Row Names.
- Before Loading Xls file we need to load the liabrary, supports xlsx.
- liabrary(xlsx) is the command to load xlsx liabrary.
#### Writing data to excel output file
It is the same syntax as we have for csv output file write function
The only difference is instead of csv, we put xlsx.
- write.xlsx(mc, "data_output.xlsx", row.names = T)

Not able to provide screenshot for reading and writing Excel Data as i am having issues with xls library function. Will fix this and update shortly. Meanwhile you can go through the commands and try to execute in RStudio.

Stay tuned for next set of commands!!!!

