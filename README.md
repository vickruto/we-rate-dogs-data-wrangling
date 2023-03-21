## Python Data Wrangling Project
### @dog_rates Tweets Data Wrangling and Analysis

The aim of the project is to gather, assess and clean the data to get it ready for downstream analysis, visualization and/or modeling. A brief preliminary analysis and visualization is included.

## The Data Used ::
 - `twitter_archive_enhanced.csv` :  A static text file containing an archive of tweets from Twitter account @dog_rates from 2015-11-15 to 2017-08-01. Available [here](https://d17h27t6h515a5.cloudfront.net/topher/2017/August/59a4e958_twitter-archive-enhanced/twitter-archive-enhanced.csv)

 - `tweet_json.txt` : Text file constructed by querying the Twitter API using Tweepy. Used to enrich the archive data with more information including the number of retweets and the number of likes

 - `image_predictions.tsv` : File containing the dog breed predictions from a Machine Learning Model. Available for download from [here](https://d17h27t6h515a5.cloudfront.net/topher/2017/August/599fd2ad_image-predictions/image-predictions.tsv)

-------  

 - `twitter_archive_master.csv` : The final master dataset stored after transforming the three data components above through all the wrangling steps

## PROJECT STRUCTURE 

.  
├── wrangle_act.ipynb <a href="https://colab.research.google.com/github/vickruto/we-rate-dogs-data-wrangling/blob/main/wrangle_act.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>
  :  ***Main Project notebook containing code for gathering, assessing, cleaning, analyzing, and visualizing data***  
├── wrangle_report.html : ***A documentation of the data wrangling steps taken: gathering, assessing, and cleaning***  
├── wrangle_report.ipnyb : ***The notebook used to generate the wrangle_report***  
├── act_report.html : ***A documentation of the insights and the visualizations produced from the wrangled data.***  
├── act_report.ipnyb : ***The notebook used to generate the act_report***  
├── no_status_tweet_ids.txt : ***Text File used to store the tweet ids that do not return a Tweet object as expected  when queried using [Tweepy](https://docs.tweepy.org/en/stable/)***  
├── twitter-archive-enhanced.csv  
├── image_predictions.tsv  
├── tweets_json.txt  
├── twitter_archive_master.csv  
└── README.md  


## Insights
The following insights were gathered from analysis of the cleaned master dataset:

1) Tweets tweeted on Wednesday are likely to get the least number of favorites and retweets while tweets tweeted on Tuesday are likely to get the highest number of favorites

2) Tweets with [`Gofundme`](www.gofundme.com)`(a crowdfunding platform)` links do not get more retweets or favorites for exposure as would be expected since WeRateDogs® is also a non-profit organization concerned with rescuing dogs and seeking treatment for sick dogs. Instead, they actually get less retweets and favorites.

3)  Tweets with videos are likely to get 5 times as many likes and 7 times as many retweets as tweets with only pictures

4) Reply tweets are likely to get half as many retweets and favorites as compared to original tweets directly tweeted by @dog_rates. However, the dogs on reply tweets on average get higher ratings at slightly above $\frac{12}{10}$ while the dogs on tweets directly tweeted by @dog_rates on average get a rating slightly below $\frac{11}{10}$
 

5) A tweet with a high number of favorite counts is likely to have a high number of retweets as well. On the other hand, the rating given to a dog does not directly predict the number of retweets or likes a tweet is likely to get.


#### Useful Links   
[Tweet Object Data Dictionary](https://developer.twitter.com/en/docs/twitter-api/v1/data-dictionary/object-model/tweet)
