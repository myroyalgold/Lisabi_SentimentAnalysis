# LISABI A LEGEND IS BORN SENTIMENT ANALYSIS
This project means a lot to me as it allows me to explain my seminar topic, 'Big Data Analytics for Decision Making,' using social media data. As a data scientist, I have been eager to use the Python programming language to perform sentiment analysis, and this project gave me the perfect opportunity to do so using a new trending movie Lisabi.

# PROBLEM STATEMENT
This project was created to test my knowledge and challenge myself on how to scrape data from Twitter using the hashtag #LisabiALegendIsBorn as a case study. I utilized the Twitter API to collect the data and performed a sentiment analysis on what people had to say about the movie released on Netflix on January 10, 2025.


# PROBLEM OBJECTIVES:
Objectives of this project include:
- Scrape data from Twitter
- Load and clean the data
- Standardize the data
- Perform sentiment analysis on the tweets
- Visualize the cleaned data
- Derive insights from the visualized data
- Make recommendations

## Task 1: Scraped Data From Twitter
This data was scraped from Twitter using Tweepy.Tweepy is a Python library that provides an easy-to-use interface for accessing the Twitter API. It allows you to interact with Twitter's endpoints, fetch tweets, and perform actions such as:
- Authentication: First, you need to authenticate with the Twitter API using your API keys and tokens.
- Fetching Tweets: Once authenticated, you can fetch tweets using methods like api.search() or api.user_timeline().
- Extracting Data: After retrieving the tweets, you can extract details such as tweet text, user information, timestamps.
- Storing Data: Finally, the extracted tweet data can be stored in a suitable format, like CSV or a database, for further analysis.
- 
## Task 2: Data Preprocessing
Data preprocessing is an essential step in the data analysis. It involves preparing and cleaning raw data to make it suitable for analysis.
After successfully retrieving the data from Twitter,
- I examined the data’s information and statistical description
- Checked for null values, and found that only the 'location' field had 78 null values, which I replaced with 'Not Specified

## Task 3: Sentiment Analysis 
Sentiment Analysis is a Natural Language Processing (NLP) technique used to determine the emotional tone behind a body of text. It helps to understand whether the expressed sentiment is positive, negative, or neutral. This is useful for analyzing user opinions, feedback, and social media content, such as tweets, product reviews, or comments.

VADER Sentiment Analysis: VADER is a lexicon and rule-based sentiment analysis tool that is specifically tuned for social media text, which tends to contain slang, emoticons, and informal language. It is particularly useful for analyzing short texts like tweets.

### Key Components in the Code:
#### NLTK (Natural Language Toolkit):
nltk is a Python library used for working with human language data (text). It provides easy-to-use tools for text processing tasks, including sentiment analysis.

#### nltk.download('vader_lexicon'):
This line downloads the VADER lexicon, which is a pre-built sentiment analysis tool included in the NLTK library. The lexicon contains a list of words that are assigned sentiment scores, ranging from negative to positive.

#### SentimentIntensityAnalyzer (SIA):
SentimentIntensityAnalyzer is a class from the nltk.sentiment.vader module designed specifically for sentiment analysis. It provides a method called polarity_scores() that computes sentiment scores for a given text.The scores include Positive, Negative, and Neutral scores.

#### Compound score:
A single value that summarizes the overall sentiment of the text. It ranges from -1 (most negative) to +1 (most positive). A score near 0 indicates neutral sentiment.

#### Sentiment Classification:
The function get_sentiment() is created to apply sentiment analysis to each tweet.
- sia.polarity_scores(tweet)['compound']: This extracts the compound score for each tweet.
- The compound score is then classified into three categories:
- Positive: If the compound score is greater than 0.05, the sentiment is considered positive.
- Negative: If the compound score is less than -0.05, the sentiment is considered negative.
- Neutral: If the compound score is between -0.05 and 0.05, the sentiment is considered neutral.

## Task 4: Visualization & Insights
- Lisabi is a movie produced by the couple Adedimeji Lateef and Bimpe Adedimeji, and directed by Niyi Akinmolayan.
- ﻿As of 3:41 PM when this data was scraped, there were a total of 100 tweets from 22 users across 8 locations, with 3:13 PM being the most frequent time for tweets.
- Conversation is largely neutral, with some positive responses and very few negative reactions.

![lisabiscreenshort](https://github.com/user-attachments/assets/b224dc8a-66a0-4090-b189-d8824fdcce94)

[LisabiReport.pdf](https://github.com/user-attachments/files/18391028/LisabiReport.pdf)

  
## Task 5: Reccomendation
Based on the sentiment analysis of Lisabi on Twitter, here are some key actions to improve engagement:
- Creating campaigns that encourage more positive reactions.
- Respond to negative comments to improve perception.
- Engage with users who are neutral to spark deeper conversations and shift their opinion.

# CHALLENGES
I faced difficulties using the Twitter API because I wasn't sure which version of the endpoint was supported by the free version. Eventually, the API tokens I generated stopped working, forcing me to start over with the coding. I spent an entire day trying to resolve the issue and, in the end, I decided to use the Bearer token. Additionally, since my previous developer account linked to my original Twitter account was set to reset on February 11, I created a new Twitter account. This allowed me to set up a new developer portal account and generate a new token, which I needed to continue explaining how to make data-driven decisions.


# LIMITATION
I used the free version of a developer account to access the Twitter API, which limits the amount of data I can pull to 100 records.
