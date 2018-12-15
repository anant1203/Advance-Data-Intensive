# Twitter-Sentiment-Analysis

Sentiment analysis is the detection of attitudes “enduring, affectively colored beliefs,
dispositions towards objects or persons”. Since long time ago, human beings have used the media
to express their needs, preferences and emotions. Internet has been one of the most used media to
make the communication possible and find information of interest. The growth of social networks
like: Twitter, Facebook, LinkedIn, and others, has generated a large amount of information about
the preferences and behavior of the users. Most of the data that is constantly generated in the social
networks could contain valuable information like point of view and tendencies of the users.
Due to exponential growth of social network, sentimental analysis has been applied to
analyze public opinion. In this project we will be analyzing sentiments of the people on the Georgia
state election 2018. We will make use of the twitter data to do our analysis. Using the data collected
we will be analyzing the sentiments by dividing the data set into two groups of Stacey Abrams,
which would be having the tweets addressing Stacey Abrams, and Brian Kemp, which would be
having tweets addressing Brian Kemp.

# Background, Motivation and Related work:

The motivation behind taking this project is to work with huge amount of data. We
started our project with collection of tweets from twitter. For collection of data from twitter we
made a developer account on twitter. We were provided with Access Token, Access Token
secret, Consumer key, Consumer Secret. Then we used tweepy API to download the tweets from
the twitter using the key provided to us. To get the tweets related to the elections we used
hashtags which were relevant to the elections recently held, such as #iamwithstacy
#teamrepublican etc. Working with huge amount of data is one of the major part of this project.
For pre-processing of the collected data, we removed emoji, regular expression and hyperlink. To
get the hidden information from the meaningful data obtained after removal.

# Technical Details:

Data collection:
To collect the data form twitter we made developer account on twitter using the access token
and is provide to us we downloaded the tweets form twitter using Tweepy. We used scripting
languages like Python for developing the essential server-side codes. We integrated our code
with tweepy to download the tweets from twitter

Data Processing /filtering :
We used R for data processing. First and foremost, we got rid of the undesired fields from
the dataset. We removed emojis, hyperlinks from the tweets for cleaning the data. The most
important point of this project was to remove the biased users as well from the dataset. For
this we did two level of processing. In the first level we simply looked at the number of
tweets per user and if the number of tweets by any user was outside the 1.5*IQR range, we
deemed that user as being biased. Basic reasoning behind this is that any user who is
unbiased would not make such huge number of tweets in such a short time span. For the
second level of removal of biased users we calculated the sentiment value for each user
based on the tweets he/she made. Then followed the same procedure of removing all the
users whose tweet score was not in the 1.5*IQR range.

Sentiment Analysis : 
Once we had biased users removed from our dataset. We calculated
the sentiment score of each user using library syuzhet in R. After getting the sentiment score
for each user we found out the maximum score, the minimum score and the mean score for
both brain kemp’s and stacey abrams’ tweets.
