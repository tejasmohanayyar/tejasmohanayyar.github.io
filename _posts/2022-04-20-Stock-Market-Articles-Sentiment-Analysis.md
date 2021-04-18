---
layout: post
title: Stock-Market Articles Sentiment Analysis using NLP and MongoDB .
excerpt: "Checking market sentiments from Feb 12th to Mar 13th."
vertical: Code
permalink: stock-market-articles-sentiment-analysis
---

<img src="images/stock/title_img.png" width="auto" height="auto" />

<center><a style = "text-align: center" target="_blank" href = "https://github.com/tejasmohanayyar/Stock-Market-Articles-Sentiment-Analysis-NLP-MongoDB"> Project on github </a> </center>

## Index of this post

* Motivation
* Methodology followed
	- Data Collection Strategy
	- Handling bad data
	- Handling missing data
	- Modelling
* Conclusion

## Motivation to do this project

Recently I have taken an interest in investing and understanding the workings of the Indian Stock Market. From what I have learnt and understood, there are
broadly two types of analysis we should do of a company before purchasing direct stocks. 

* Fundamental Analysis
* Technical Analysis

**Fundamental Analysis**

This deals with the performance and future prospects of the company alone. It involves analyzing the overall company performance and future growth prospects. Under this type of analysis we would look at the companies cash flow statements, annual reports and their overall management.

**Technical Analysis**

This type of analysis purely deals with the performance of the stock in the market. We would analyze the different candle stick patterns, look for patterns like double bottom or the tea cup pattern etc. We also look at various metrics like the Stocks P/E Ratio, EPS, P/B Ratio, standard deviation, alpha which tells the performance of the stock vs the index and beta which gives us a picture of volatility and risk. There are many more parameters that must be looked at within technical analysis but as of now I have come accross only these metrics.

**Overall Market News**

After performing the above two analysis and picking your basket of stocks, it is also important to follow the news and understand about how these companies are performing. For this I have created a project which is scrapping news articles from the Economic Times to figure out overall news about the share market. Since I have started my investment journey through index funds I prefer to look at the overall market sentiment. This project does just that. It scouers through the articles and looks for key words which allow our algorithms to determine whether a news article is positive or negative. The implications of this could be used as a decision factor in whether to invest in the index at a certain time or not. For instance with high positive news, there is a chance that the index is doing very well on that day. Looking at previous articles we can see how the market did the following day and try to find patterns so that we can get an expectation of how the market performance the  next day based on previous day market sentiments.

## Methodology followed

### Data Collection Strategy

* From the website  that I was collecting data, they had blocked access to libraries like urllib and url request. The only way to access the website was through a browser. So I decided to use the **Selenium** python library that would access the website via a browser and I could also code the entire scrapping process in python. 

* Using **BeautifulSoup** I have passed the output of selenium which is raw html into an html parser. This makes it easier to access each tag in the html which we will use to extract all the relevant data. 

* I have collected 3 features:
 - Date article was posted
 - Article Headline
 - Article Summary
 - Article URL

* From the article url using requests, I am accessing each article page and scrapping data from each article. 

* I in no way encourage people to do webscrapping and understand that the hosts server faces the load. Hence I am safely scrapping 40-50 records every 2-3 days to ensure I am not bombarding the hosts system.

### Handling Bad Data

**Webscrapping issues and challenges:**

* The economic times loads more articles as we scroll which is why I could not use requests since it does not give us page movement features. 

* To load more news articles, the "load more articles" button is to be pressed and is located after all articles. For this I had to first center that button on the screen and then press the button. All of this was done in code.

* Scrapped data was saved in a MongoDB database in my local system for future use.

### NLP Preprocessing

**Libraries Used**
* NLTK
* re
* string

* NLP Preprocessing like converting articles to lowercase, replacing percentage, removing_punctuations, removing_stop_words and removing_numbers all took time to process since these are big articles over which we are applying all these transformations.

* Lemmatization was done for the words in articles to increase more words being common among the articles. The advantage of lemmatization is that it preserves the meaning of the word as opposed to stemming which would chop of words without looking at whether the obtained new word is part of the origin language or not.


### Handling Missing Data

* **Articles** was the only column that had missing data. Since it was only 8%, I replaced the full article with the summary of the article which got captured.

### Exploratory Data Analysis

* **Visualization of the most frequently occuring words was done**

<img src="images/stock/freq.png" width="auto" height="auto" />

### TF-IDF

For converting the articles into number form, I manually converted the articles into numbers using the TF-IDF methodology. For better understanding I have written code for the same from scratch.

<Make changes from here>
##########################################################################################################################################################

### Unsupervised Machine Learning



## Conclusion

* I got hands-on experience in webscrapping, EDA, Feature Engineering, Feature Selection, ML model building, pandas, numpy, Bootstrap 4, Flask, git, stats, object oriented programming, versioning of files and keeping each version, geocoding location data, creating seperate html files and calling them from flask, pycharm, json, pickle and joblib for saving models,scikit-learn, xgboost, cross validation, grid search CV.

* My intership of 4 months at Sunteck Realty gave me enough domain knowledge to handle certain features and have a strong grip over what I was doing since I was able to understand most of the real estate terminologies like carpet area, super area, loading, RERA etc. I also had descent knowledge on the prices of houses in area's where Sunteck has their projects since all of us interns had shared this information about the projects with each other. 

* You can also check out this 
<a style = "text-align: center" target="_blank" href = "https://github.com/tejasmohanayyar/webscrapping-and-predicting-mumbai-property-prices"> Project on github </a> and also the <a style = "text-align: center" target="_blank" href = "https://mumbai-property-price.herokuapp.com/">Web app</a>. 

Thank You for reading.




