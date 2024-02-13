# Sentiment-Analysis-for-Financial-Tweets
Sentimet Analysis for finacial tweets from Cashtag Piggybacking dataset (https://zenodo.org/records/2686862) which includes ~9M tweets mentioning stocks (cashtags) traded on the most important US markets, shared between May and September 2017 and financial information about ~30k companies found in those tweets, retrieved from Google Finance.

I have attempt the analyze statistics of the tweets making 4 different sentiment analysis models to label the tweets as positive and negative. The cumulative results of the sentiment analysis are then used to find whether if there is any correlation between the sentimnet behind a cashtag and its price movements.

Explanations of each Notebook are as follows:

### Visualization Notebook
In this notebook, I have tried to understand the statistics of all tweets, deviding them into different market's different time zones. The visualizations can give you a good understanding of:

• Statistics on most and least tweeted stocks and segmentation of the
companies based on the number of tweets they have.

• Statistics on distributions of 5 important stocks refelecting different sectors of the economy over time.

• Statistics on distributions of all financial tweets over time.

• Statistics on distributions of retweets per tweets over time.

• Statistics on most important financial information on individual stocks computed solely from the financial information (not tweets).

• Time series movement directions through time for individual stocks and the reason behind these directions from real world news.

• Co-occurrence of various stocks in the same tweets.

### Sentimet Notebook
In this Notebook, I have developed 4 different sentiment analysis models including BOW(Bag of Words), TFIDF, BERT and, ROBERTA(https://huggingface.co/docs/transformers/model_doc/roberta) models.

The preprocessing of tweets include removing hastaghs, cahstags, urls, mentions and stop words. After this lemmitization is done for the tokens of the tweets in ordwr to make them more compatible with the models.

The models achieved up to 80% accuarcy on the test set which was a custom dataset of tweets. The best model was the trained ROBERTA model.

### Correlation Notebooks
In this Notebook, I calculate the correlation between the average snetiment of tweets for each cashtag and their preformance in the datasets duration. Two correlations, Pearson and Spearman, are used.

Also the correlation of the number of tweets and the sentiment of the tweets are calculated as well.

The results reveal not much of a correlation between the sentimet behind a cashtag and its preformace. The correlations are arounf ~0.1 with a high p-value indication not a significat correlation between the two againt our expectations.

This converges with results from most of the economic studies where the obvoius result appears to be wrong or non-significant. This mostly happens because of the massive amount of noise in tweet data, small window of study and most importantly because of the fact that we are dealing with financial markets and if such an correlation existed it would have been found and arbitraged a while ago making it ineffective. The reason for this matter is that financial markets are second degree complex systems and information about the market changes the behavior of the market.

## Contributers
Pouya Farivar        pouyam.fr@gmail.com
