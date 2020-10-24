---
layout: post
title: Building an image scrapper for collecting image data.
permalink: image-scrapper

---
|Reading images on google|Saving images|
|----|-------|
|<img src = "/images/deployment/review1.png">|<img src = "/images/deployment/review2.png">|
|--|--|


<center><a href = "https://github.com/tejasmohanayyar/google-images-scrapper" target = "_blank">All files on github</a></center>

## Why build this app?

* I wanted to learn image scrapping, and needed a tool to scrap images for projects with Neural Networks like object classification projects.

* This project seemed to me as the ideal mix of whatever I wanted to learn while also building a useful tool for myself. 

* I have no intentions of commercializing this product and have only made this for learning purposes. 

## Overall functionality

* The app will expects the user to enter the term to be searched in the program and also the number of images to scrap.

* Then the images are saved on the local system within a folder named as the search term.

## Tools used

* Pycharm Community edition 2020.1.1
* Python 3.6.12
* chrome driver (according to chrome version)


## Main Libraries used. (Rest in [requirements.txt](https://github.com/tejasmohanayyar/google-images-scrapper/blob/master/requirements.txt))

* Selenium: For controlling my computer applications remotely like opening the browser and going through each image.
* OS: To handle the file system.
* time: To introduce delay.
* Requests: To open links of webpages.


Thank You for reading this post. If this post helped you out in anyway reach out to me on twitter and let me know! Thanks.