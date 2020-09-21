---
layout: post
title: "Merging multiple excel sheets and converting all features into a common format."
permalink: "ETL-leads-project"

---

<img src = "/images/talend-images/talend_project.png">

The project here was done in my final year of my MBA Tech course at NMIMS. The subject name was ETL where we were taught to handle data using excel and Talend by Prof. Cyrus Lentins. This project was done in Talend and was our final submission before we completed the course. Below you will find all the steps that were performed to achieve this project along with screenshots of all the steps.

### Procedures follwed before creating a talend job:

* After creating a new project, go within its folder and create a Data folder. Here we will store our input and output files. 
* Right click on job designs and select create a new job. 
* Then we create schema's for input and output files.
* Now we can start creating our talend job in the designer.

### About the data:

* The datasheet can be found here.
* It consists of 3 sheets which have the same columns but the data are in different formats in each sheet.
* Our job is to change all the data to have a uniform format and finally merge all the 3 sheets. We are also supposed to create a new column that tells the end user from which sheet the data has come.

### Screens of the initial dataset

|Telephone|WebChat|WebForm|
|---|---|---|
|<img src = "/images/talend-images/talend_project1.png">|<img src = "/images/talend-images/talend_project2.png">|<img src = "/images/talend-images/talend_project3.png">|

### Screens of the output Obtained

<img src = "/images/talend-images/talend_project4.png">

### Procedure followed:

#### Modifying the telephone sheet: 

|Input|Tmap|Output|
|---|---|---|
|<img src = "/images/talend-images/talend_project5.png">|<img src = "/images/talend-images/talend_project6.png">|<img src = "/images/talend-images/talend_project7.png">|


#### Modifying the WebChat sheet.

|Input|Tmap|Output|
|---|---|---|
|<img src = "/images/talend-images/talend_project8.png">|<img src = "/images/talend-images/talend_project9.png">|<img src = "/images/talend-images/talend_project10.png">|

#### Modifying the WebForm sheet.

|Input|Tmap|Output|
|---|---|---|
|<img src = "/images/talend-images/talend_project11.png">|<img src = "/images/talend-images/talend_project12.png">|<img src = "/images/talend-images/talend_project13.png">|

#### Converting the csv file to xlsx.

|ReadCSV|Writexlsx|
|---|---|
|<img src = "/images/talend-images/talend_project14.png">|<img src = "/images/talend-images/talend_project15.png">|

### Project files:

The project files can be found [here](https://github.com/tejasmohanayyar/tejasmohanayyar.github.io/tree/master/projects/ETL-Projects/Final%20Project)

### Conclusion:

* In the end we were able to use Talend to merge the given 3 sheets into a common format. This project was a medium to test our skills that we had learnt in the course covering close to 80% of all the concepts picked up.
