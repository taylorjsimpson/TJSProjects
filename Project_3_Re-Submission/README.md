# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) How to Increase Tourism in Boston: A presentation to the Massachusetts Board of Tourism

## Project Authors
| [Taylor Simpson](https://github.com/taylorjsimpson) |


## Table Of Contents
[1. Problem Statement](#1.-Problem-Statement)<br>
[2. Executive Summary](#2.-Tools-&-Methodology)<br>
[3. Data Dictionary](#3.-Data-Dictionary)<br>
[4. Key Takeways](#4.-Key-Takeaways)<br>
[5. Next Steps](#5.-Next-Steps)<br>

## 1. Problem Statement

The Massachusetts Board of Tourism tasked me with figuring out the best way to increase tourism in the city of Boston. While traditional methods typically tend to use more traditional approaches, the novelty of this approach is using new forms of online media and advertising to increase tourism.


## 2. Executive Summary

Data was gathered from the internet for tourism numbers and webscraped Reddit for the most popular Subreddits and key terms for Boston, competitor New York City, and a Memes page for an analysis that we ended up going in a diferent direction with. Over 5000 Subreddits were scraped and analyzed for most common words related to the city.
A for loop was written to fill a dictionary with posts, and bag of words, count vectorizer, and StopWords were used to ensure most common words for each Reddit used. 

Using the Reddit data, a sueprvised learning Logistic Regression Model was built to determine what Subreddit web visitors were on.


The following packages were imported to conduct this analysis.

|                |            |                |              |            |                |
|----------------|------------|----------------|--------------|------------|--------------- |
| Pandas         | Matplotlib | Scipy          | Sklearn      | Numpy      | TFIDVectorizer |
| Beautiful Soup | Log-Ref    | CountVectorizer| GridSearchCV | Statsmodel | Pipeline       |
                   


## 3. Key Takeaways

Using stop words we were able to get rid of the most common words that would not be helpful to modeling and were able to use bag of words to create an entire dictionary of words most common in the Boston, New York City, and Memes subreddits. Using a GridSearched CountVectorizer were able to run a Logistic Regression Model with accuracy scores of over 80, and tested with sample text that confirmed model could accurately predict which SubReddit words are in. This was integral as we could make recommendations using this. 

## 4. Recommendations and Next Steps

As Reddit is a very community and "Internet" oriented website our recommendations are to make sure to meet them at their own level so to speak, which first off means no standard corporate ads. One thing Redditors appreciate are Ask Me Anythings. "AMA's" are events when celebrities from all fields of sports, entertainment, media, government, technology, and business make themselves available for designated time periods to answer almost any and all questions members of Reddit have. We also would advise offering some type of free giveaway, either Boston stuff or a trip to the City on a Hill. There also are targeted Reddit ads could do, similar to Google Ads. The results of our analysis showed that it would be a good idea to emphasize the neighborhood aspects and commute-ability of Boston as both of those were most common features. 
