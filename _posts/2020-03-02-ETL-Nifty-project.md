---
layout: post
title: Extracting columns out of Nifty dataset and creating our own columns using Tmap
permalink: ETL-nifty-project

---

<img src = "/images/talend-images/talend-m23.png">

This project was done in Talend as part of our course curriculum at NMIMS in my final year. The objective here was as follows:

### Refer to file “20181019-ETL-Test2-Nifty.csv”

Make a Talend Project to carry out the following: 

* Create new .csv file to contain on the following fields:

|1|2|3|
|---|---|---|
|RefId|	Security|	HghPrice|
|RecDate|	PrevClose|	LowPrice|
|Symbol|	OpenPrice|	ClosePrice|

* Create new column “PoL” as “ClosePrice” – “PrevClose”.
* Create new column “PoL-Label”
* PoL-Label should contain “Profit” where “PoL” > 0
* PoL-Label should contain “Loss” where “PoL” < 0
* PoL-Label should contain “Zero” where “PoL” = 0

Procedures follwed before creating a talend job:

* After creating a new project, go within its folder and create a Data folder. Here we will store our input and output files. 
* Right click on job designs and select create a new job. 
* Then we create schema's for input and output files.
* Now we can start creating our talend job in the designer.

### Input:

<img src = "/images/talend-images/talend-m21.png">

### Talend Screens:

|Input|Tmap|Output|
|---|---|---|
|<img src = "/images/talend-images/talend-m22.png">|<img src = "/images/talend-images/talend-m23.png">|<img src = "/images/talend-images/talend-m24.png">|

### Final Output:

<img src = "/images/talend-images/talend-m25.png">

### Project files:

You can also download the .csv file [here](https://github.com/tejasmohanayyar/tejasmohanayyar.github.io/tree/master/projects/ETL-Projects/ETL%20Nifty%20project)

### Conclusion:

* This project allowed me to clear all my concepts and apply them practically. I was able to use if statements in tmap and also create and remove columns in tmap.

* I was also able to create Schema's for a delimited file in Talend. 

* Got an understanding of how tmap works and its capabilities.


