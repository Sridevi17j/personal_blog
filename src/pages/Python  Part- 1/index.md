---
title: Python- Part 1
date: "2020-06-26T22:12:03.284Z"
---
After installing python and Jupyter Notebook, now start your Jupyter notebook from the terminal which runs in port 8888 in the localhost. Now lets start with python programming.    
### Import Libraries
import os  
import pandas as pd  
import numpy as np  
import matplotlib as mlt 
### Set working Directory
We have to call inbuilt functions using the libraries. 
import os  
os.chdir("/Users/mac/Desktop/new/Python")- Set Working Dir
os.getcwd() - Get current working Dir
### Screenshot for above commands
![](./p1.png)
Note:- Shift+Enter to run your commands
When i tried to import pandas library, i got an error " No modules named pandas" Which i fixed by installing pandas under bin, before importing it, and below is the command.    
pip install pandas
### Using operators- Basics
![](./p2.png)
### Python Math-Calculations
Some math calculations using library called math.
![](./p4.png)
### Defining function and calling the function
It is same like other programming languages, only few syntax gets varied. But its very easy to learn. Check some basic easy defining and calling functions.
Used int, and str as passing parameters. You can use any variables, using the same syntax.
![](./p3.png)

There are more and more basic commands , From next post, we will start to learn commands related to DataScience like loading csv, excel files and read/write files.





