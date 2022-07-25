# tweeter_covid19_NLP
Covid 19 Tweeter Analysis using Natural Language Processing techniques.
### 1. Collecting the Twitter messages

Twitter has provided Tweeter API to extract tweets for various text and other analysis using Twitter data. In order to extract specific Tweets which related to Coivd-19 I have used following #hashtags for Tweets.
keywords ="#covid19 OR #covid 19 OR #COVID 19 OR #covid OR #corona OR #coronavirus OR #novelcoronavirus OR #newcoronavirus OR #SARSCoV2 OR 2019 nCoV OR SARS CoV 2 OR
#socialdistancing OR #PhysicalDistancing OR #facemask O R #StayHome OR #StayHomeStaySafe OR #lockdown OR #LockdownNow OR #QuarantineandChill OR #quarantine OR #pandemic OR
#PCR OR #

#### Data extraction using Python and Twitter API
Following illustrate the code block which use to extract the relevant Tweets for Twitter
![image](https://user-images.githubusercontent.com/85073848/179394400-2bf6eaea-6e93-411f-ae75-61a4a987a829.png)
![image](https://user-images.githubusercontent.com/85073848/179394377-f2ae827b-c741-4748-82f8-654fdf97f4e6.png)
#### Sample JSON output
![image](https://user-images.githubusercontent.com/85073848/179394459-a76ed8fa-c087-4127-bb9b-229b2f5b7105.png)

However, Twitter will allow only 1 API call every 15 mins and only 200 tweets will pass as JSON. Therefore, extracting over 5000 tweets for the analysis is not feasible to schedule API call and add the data to make big dataset.
Hence, for the above analysis I have used “COVID19 Tweets” dataset from www.kaggle.com website.

Above dataset contains 179,108 data points and 13 features including [user_name, user_location, user_description, user_created, user_followers, user_friends, user_favourites, user_verified, date, text, hashtags, source, is_retweet]
Link to the dataset:
https://www.kaggle.com/gpreda/covid19-tweets

###2. Identify the distribution of tweets in the world map

####What are the techniques that you use to map the tweet to a relevant country?
Provided dataset already had the location column either a country or city, state of the tweet. Hence use mainly geo panda’s python library to take the county, city and state to convert them to the Country code. Then it has been converted to country names and plot the data in a bar chart and visualize it in a choropleth world map to show the demographic distribution of the tweets with heatmap.

For above analysis I have used google colab jupyter notebook to process the code more efficiently. Since it is an cloud environment it provided fast and more processing power to run the NLP algorithms required.

![image](https://user-images.githubusercontent.com/85073848/179394588-b5f47dc0-11ea-4135-9251-8d6388a19d94.png)

![image](https://user-images.githubusercontent.com/85073848/179394653-950084f5-458e-44d5-af3d-53b896da0de0.png)

Up to above step, location column was counted and sorted for first 15 top locations were reported in the dataset. Still some of the states and cities are shown as separate locations.

Using “Geo Text” states and cities were converted in the country codes

![image](https://user-images.githubusercontent.com/85073848/179394681-6ae07cf2-2d83-430a-bdbf-e6ac188a03df.png)

![image](https://user-images.githubusercontent.com/85073848/179394708-706cde78-33a1-498b-9097-414d673ec055.png)

![image](https://user-images.githubusercontent.com/85073848/180847467-d14fb0e3-4c81-470a-b210-7cf3fa5f5b86.png)




