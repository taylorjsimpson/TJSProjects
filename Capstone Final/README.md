# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Predicting Movie Revenue

## Project Author
 [Taylor Simpson](https://github.com/taylorjsimpson) |

## Contents of Repo

<!--ts-->
* [Code](http://localhost:8888/tree/CCCI_4)
  * [Data Collection & Data Aggregation](http://localhost:8888/notebooks/CCCI_4/code/Data%20Collection%20and%20Cleaning%20.ipynb)
  * [Exploratory Data Analysis]
  (http://localhost:8889/notebooks/CCCI_4/code/EDA.ipynb)
  * [Supervised Learning Regression Model](http://localhost:8889/notebooks/CCCI_4/code/Supervised_Learning_Regression_Models.ipynb)
  * [Supervised Learning Classification Model](http://localhost:8889/notebooks/CCCI_4/code/Supervised_Learning_Classification_Model.ipynb)
  * [Master Copy]
  (http://localhost:8888/notebooks/CCCI_4/code/Beginning%20to%20End%20Code.ipynb)
* 
<!--te-->

## Table Of Contents
[1. Problem Statement](#1.-Problem-Statement)<br>
[2. Executive Summary](#2.-Tools-&-Methodology)<br>
[3. Data Dictionary](#3.-Data-Dictionary)<br>
[4. Key Takeways](#4.-Key-Takeaways)<br>
[5. Next Steps](#5.-Next-Steps)<br>

## 1. Problem Statement

For my capstone project I will build linear and logistic regression models to predict the opening weekend box office and total revenue for a movie release. These models will provide insight of what features (genre, runtime, critical rating, user rating, release date, etc.) are most predictive of a movie’s financial success. I plan on using linear to get a discrete prediction and logistic to predict whether or not it will cross a certain threshold ($5 million). Three statistics will be used to evaluate model fit: R-squared, the overall F-test, and the Root Mean Square Error (RMSE)


## 2. Executive Summary

Data was gathered from Movie Lens for over 45,000 movies. The data was categorically divided into multiple categories, 
       'Adult', 'Belongs To Collection', 'Budget', 'Genres', 'Homepage', 'ID',
       'IMDB_id', 'Original Language', 'Original Title', 'Overview',
       'Popularity', 'Poster Path', 'Production Companies',
       'Production Countries', 'Release Date', 'Revenue', 'Runtime',
       'Spoken Languages', 'Status', 'Tagline', 'Title', 'Video',
       'Vote Average', 'Vote Count' which totaled almost 45,000 datapoints.  

Using the Kaggle data, supervised and unsupervised learning models were built to predict revenue and identify patterns in the data.



The following packages were imported to conduct this analysis.

|                 |            |         |           |            |            |
|---------------- |------------|---------|-----------|------------|------------|
| Pandas          | Matplotlib | Seaborn | Sklearn   | Numpy      | Requests   |
|Linear Regression|  Logistic  | Random  | Metrics   | Plotly     | Statsmodel |
|Datetime         | Regression | Forest  | GridSearch| ExtraTrees | r2Score    |



## 3. Data Dictionary

Sources:
* https://movielens.org/


|Feature|Type|Description|
|Adult|object|Whether or not a movie is "Adult"|
|Belongs To Collection|object|Description|
|Budget|object|Number of dollars it cost to make|
|Genres All|object|List of up to three different categories movie falls under|
|Homepage|object|Link to website|
|ID|object|Unique key identifier for MoviesLens|
|IMDB_id|object|Unique value key for IMDB.com|
|Month|object|Month of year movie released in|
|Original Language|object|Language of movie |
|Original Title|object|Name of movie|
|Over 5 Million|float64|Yes/No of if movie released grossed more than $5 million|
|Overview|object|Short summary description of plot|
|Popularity|float64|Description|
|Poster Path|object|Link to website that shows Poster of movie|
|Primary Genre|object|First genre listed in description|
|Production Companies|object|Companies that funded movie|
|Production Countries|object|Country where movie was released|
|Release Date|Type|Month/Date/Year movie was released|
|Revenue|float64|Overall amount of money movie grossed in theaters|
|Season Released|object|Time of year movie was released - Winter = 1, Spring = 2, Summer = 3, Fall = 4|
|Spoken Languages|object|Languages spoken in movie|
|Status|object|Released or not released|
|Tagline|object|Tagline of movie in ads|
|Title|object|Final released title|
|Video|object|Yes/No on if movie was released on Video|
|Vote Average|float64|MoviesLens users rating on scale from 1-10|
|Vote Count|float64|Number of MovieLens users that voted up to 14,000|




## 4. Key Takeaways

After running a Seaborn correlation Heatmap the most important features were Vote Count and Budget.

The linear regression model that was created was overfit and had a score of 73 and adjusted r squared of 77. 
The logistic regression model that was created was better but still overfit, with a score of 82.
The Random Forest model was by the best, far less underfit and a score of 84 and my model able to make 5/6 predictions correctly.  

## 5. Next Steps

Next steps would first be to go back and supplememt my dataset, one thing I would be interested in getting would be being able to quantify star power of actors involved, using prior box office performance and screen time. 

Also I want to do more genre analysis using K Nearest Neighbors and run a Principle Component Analysis Model.
