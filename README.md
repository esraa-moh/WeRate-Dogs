# WeRate-Dogs
Udacity Data Analysis 
The WeRateDogs Project This report describes the steps i made to complete the Data Wrangling project

1-Gathering Data Gathering is done by obtaining 3 Datasets from 3 different sources

First i downloaded the twitter-archive-enhanced.csv manually from the courses resources .

The second dataset i downloaded is the image-predictions.tsv by using requests library and get() method using the given url as parameter

The third dataset is downloaded from twitter api using Tweepy library after i created a twitter developer account , i used the api key ,consumer key , access token and access secret to query the json data with respect to the rate limit and saving the data in text file called tweet_json.txt saving only tweets which have id , and i made a dictionary by reading the file line by line and then made a dataframe for just the retweet_count and favorite count of each tweet

2-Assessing I started a visual assessing by opening each dataframe on the jupyter notebook using panadas library and i opened a copy of each file on google sheets for more assessing , i wrote the issues i found on a summary ,and after that i started to making assessing programmatically using jupyter notebook using dataframe info() , value_counts() , duplicated() and other pandas methods

Some quality issues are observed like None string values instead of numby nan and dataset contain retweets and replies beside original tweets , and some wrong data types as timestamp which was object instead of datetime, Dogs names with Weired values and incomplete names also in the image predictions table an issue of wrong predictions and unnecessary columns and other issues based on checking Completeness , Validity ,Accuracy and consistency

Some Tidiness issues are observed like 4 columns to describe dog class and other issues observed based on the tidiness rule that each variable should represent a column and each observation represent a row and each observational unit forms a table

All issues are written for Assessing summary to help in cleaning process

3-Cleaning Each issue in the assessing stage is cleaned by first defining the issue and how to solve it , and second by solving it by code and then test the data after solving the problem

I used the pandas functions to solve the issues programmaticaly and to test the data ,and some issues are solved manually as weired dog names , and after that i merged the three tables into one table with only original retweets and necessary columns

After that the clean dataframe is stored into twitter_archive_master.csv to make further Analysis and Visualization for it
