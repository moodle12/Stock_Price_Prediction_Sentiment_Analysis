# Project Description:

This project is about analyzing social media data about Apple Inc. and predicting its future stock trend with sentiment classification.
I applied sentiment analysis and machine learning principles to discover the possible effect of "public sentiment" on "market trends".

Prediction of stock price is an extremely complex and very challenging task because there are too many factors involved such as economic circumstances, political events, and other environmental factors which may impact the stock price.
Due to these factors, it is difficult to find out the dependence of a single factor on future prices and trends.

The popularity and importance of numerous social media platforms has risen to new levels over the past few years, as more people spend time online.
One such social media platform that has seen an explosive rise in popularity is Twitter. Twitter is a rich source of real-time information regarding current societal trends and opinions.

Dataset: https://www.kaggle.com/datasets/nadun94/twitter-sentiments-aapl-stock

Twitter data from Kaggle for Apple stock was used for sentiment analysis. The time frame chosen to analyze data is January 01, 2016 to August 31, 2019.

Collected daily Apple stock data for the same time period from Yahoo Finance for historical data analysis and stock price/trend prediction.

Twitter information was processed to use only data for the dates the stock market was open (approximately 252 trading days per year).

Twitter Data and Daily stock prices were merged together and a final csv was generated which was used as base data. For all the predictive analyses, have used the adjusted close price of AAPL.

# Model training and evaluation

Different machine learning techniques were used to train and evaluate models to analyze and determine the correlation between twitter sentiment and Apple stock price.

Two approaches for analyses were used:

Classification: In this approach the twitter polarity scores were used to classify tweets into positive, negative and neutral sentiment. The adjusted closing prices of Apple stock were converted to a binary form (0 and 1), where 0 means that the value of the company stock price is less than the day before, and 1 means that the value is greater than the day before. This provided a trend for stock price movement.

Algorithms used for analysis:

Random Forest Classifier

Random Forest Classifier is an ensemble method, meaning that a random forest model is made up of a large number of small decision trees, called estimators, which each produce their own predictions. The random forest model combines the predictions of the estimators to produce a more accurate prediction.

Gradient Boosting Classifier

Gradient Booster algorithm builds trees one at a time, where each new tree helps to correct errors made by previously trained tree. With each tree added, the model becomes even more expressive. There are typically three parameters - number of trees, depth of trees and learning rate, and each tree built is generally shallow.

Regression: In this approach the twitter polarity scores, twitter volume and the adjusted closing prices were used to predict the future movement in Apple stock price. The adjusted closing prices data was stuctured such that previous time steps were used as input variables and the next time step as the output variable.

Algorithms used for analysis:

Random Forest Regressor

Random Forest Regression is a supervised learning algorithm that uses ensemble learning method for regression. Ensemble learning method is a technique that combines predictions from multiple machine learning algorithms to make a more accurate prediction than a single model.

LSTM RNN

Long short-term memory (LSTM) is an artificial recurrent neural network (RNN) architecture used in the field of deep learning. LSTM networks are well-suited for making predictions based on time series data, since there can be lags of unknown duration between important events in a time series.

XGBoost Regressor

XGBoost is short for Extreme Gradient Boosting and is an efficient implementation of the gradient boosting machine learning algorithm.


With Accuracy scores in the range of 50-55%, the classification approach did not yield much confidence so as to justify usage to correlate stock movement with Twitter Sentiments.



Using the regression approach yielded favorable results as against classification. These models relied heavily on the previous prices and as is visible from the trends, Twitter sentiments were not accurately indicative of stock price movements. The XG Boost regressor was observed to be the optimum model to simulate future prices.

# Limitations/ What could have been done differently?

Twitter API has limitations on the amount of data that can be accessed. Therefore, a document with Twitter information regarding Apple stock from Kaggle was used.

The Kaggle dataset also had limited data (Jan'16 - Aug'19) which restricted my analysis to limited number of trading days.

NewsAPI headlines besides Twitter could also have been used for sentiment analysis.
