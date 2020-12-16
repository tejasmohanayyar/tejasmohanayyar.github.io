---
layout: post
title: Real Estate price prediction for Mumbai properties with deployment
permalink: Real-estate-price-prediction
---
<img src="images/real estate/realestatedeployed.gif" width="auto" height="auto" />

<center><a style = "text-align: center" target="_blank" href = "https://github.com/tejasmohanayyar/real-estate-price-prediction-end-to-end-project-with-deployment"> Project on github </a> </center>

<center><a style = "text-align: center" target="_blank" href = "https://secure-headland-42412.herokuapp.com/"> Web app link </a> </center>


## Index of this post

* Motivation
* Methodology followed
* Data Collection
* Feature Imputations,Engineering and Visualization
* Modelling
* Deployment

## Motivation to do this project

I had pursued a 6 month internship at Sunteck realty ltd. from May to September 2019. There I was in the Sales and marketing team but for a brief part of the internship I was part of a team responsible for doing some Market Research at Sunteck Westworld located in Naigaon. The research was related to brand preferences of people. The domain knowledge I gained there came in handy while doing this project. Though this project does not look at brand preferences but I was curious about Mumbai's real estate market and wanted to create a price predictor for every location in Mumbai. This would help any user to asses the value of their flat in the year 2020. 

## Methodology followed

* Data Collection
* Feature Imputations,Engineering and Visualization
* Modelling
* Deployment
* Conclusion
* Libraries Used in this project


## Data Collection

* Data was webscrapped by me from a real estate website using BeautifulSoup and Selenium. The notebook to which can be found [here](https://github.com/tejasmohanayyar/real-estate-price-prediction-end-to-end-project-with-deployment/blob/master/scrapped%20magicbricks/scrapping%20magicbricks.ipynb).

* I let the code run for around 1.5 hours  and scrapped 2500 datapoints and 20 features from the website. It took 2 hours because I had added a delay for each selenium scroll instance during the scrapping process to not create much of a load for the website.

## Feature Imputations,Engineering and Visualization

* The next step was to transform the datapoints into a form that would be most suited for ML and creating visualizations. That notebook can be found [here](https://github.com/tejasmohanayyar/real-estate-price-prediction-end-to-end-project-with-deployment/blob/master/scrapped%20magicbricks/Feature%20imputations.ipynb).

* The notebook for feature engineering and visualizations can be found [here](https://github.com/tejasmohanayyar/real-estate-price-prediction-end-to-end-project-with-deployment/blob/master/scrapped%20magicbricks/Visualization%20and%20feature%20engineering.ipynb).

* Post all my findings from the above notebook I have dropped some features and finally we end up with 8 features. Initially we had 20 features.

##  Modelling

* I have used Linear Regression, Ridge, Lasso, ElasticNet and Random Forrests to create my algorithm. Random forrest performed the best for me. This is expected since random forest uses multiple decision trees and gives a majority result. Multiple models mostly perform better than a standalone model. Although in this case the difference in accuracy was not too high.

* The jupyter notebook for modelling can be found [here](https://github.com/tejasmohanayyar/real-estate-price-prediction-end-to-end-project-with-deployment/blob/master/scrapped%20magicbricks/Modeling.ipynb).

## Deployment

* For deployment I have written some bare-bones html and css to demo this app. 
* I have also used the flask API in a python script which can be found [here](https://github.com/tejasmohanayyar/real-estate-price-prediction-end-to-end-project-with-deployment/blob/master/app.py).
* Finally I have deployed the app on heroku, the link to which can be found [here](https://secure-headland-42412.herokuapp.com/).


## Conclusion

* This project helped me learn and implement webscrapping and deployment skills.
* I was also motivated to get practical experience in most facets of the ML pipeline particularly Data Collection, Feature Engineering, Data Visualization, Modelling using ML algorithms. You can find the full github repo [here](https://github.com/tejasmohanayyar/real-estate-price-prediction-end-to-end-project-with-deployment).

**Libraries used in this project:**

- beautifulSoup
- selenium
- pandas
- numpy
- matplotlib
- seaborn
- folium
- plotly
- scikit-learn
- statsmodels

