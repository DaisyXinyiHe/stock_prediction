# stock_prediction

## Introduction
  Stock market prediction is an interesting mathematical problem that was explored by many researchers. To predict a stock means using the present or past values of a stock’s features, such as its prices and related events, to predict the future value of a stock. 
  In this project, I explored two different traditional methods in stock market prediction: time series analysis and market sentiment analysis. The major difference between these two methods was that in time series analysis, past stock performance were the main predictors of the future stock performance; while in market sentiment analysis, market sentiment was the main predictor of the future stock performance. 

## Data
 
### Kaggle Dataset on DJIA and Reddit World News
  For this project, I used a Kaggle dataset which included the Dow Jones Industrial Average from August 8th, 2008 to July 1st, 2016 and Reddit news from June 8th,  2008 to July 1st, 2016. The dataset could be found in this link: https://www.kaggle.com/aaron7sun/stocknews . 

  The Dow Jones Industrial Average (DJIA) tracked the stock market performance of the United States by tracking the stock price of thirty most outstanding companies in the United States. As a price-weighted measurement, the DJIA consisted of companies from different sectors. The majority of the companies in the DJIA index were multinational companies, which means that they had business operations outside of the United States. The dataset included the opening price of the date, highest price of the date, lowest price of the date, and the trade volume of the data. 

  The news dataset contained the top 25 historical news headlines ranked by reddit users' votes from June 8th,  2008 to July 1st, 2016 from the Reddit WorldNews Channel. The total number of headlines was 73,608. The content of the news headline not only included news from the United States, but also news from other countries. 
  
## Measurement
 
### Stock Market Performance Measurement
Calculate the percentage of change in closing price as stock return:
Stock Price Change Percentage = (Closing Price<sub>t</sub> - Closing Price<sub>t-1</sub> )Closing Price<sub>t-1</sub> * 100

### Model Performance Measurement: RMSE
In time series analysis, measuring model prediction accuracy became tricky when it came to a non-classification problem like predicting stock market performance. In this project, I calculated the root mean square error (RMSE) to measure the model performances

## Methods 
The following methods were considered in this project :
- Time Series Analysis
  * ARIMA
  * Generalized Autoregressive Conditional Heteroskedasticity (GARCH)
  * State-space model with Kalman Filter and Expectation Maximization
- Market Sentiment Analysis
  * Flair’s pre-trained sentiment analysis model to classify sentiment in news headlines. 
  * Linear regression to examine the correlation between sentiment and market movement. 

### Training and Testing Dataset
In order to measure the performance of the methods, I splitted the data into a training set and a testing set. The training set contained the first 80% of the dataset and the testing set contained the rest of the 20% of the dataset. In order to preserve the time order, I did not randomize my sampling process. 

### Pre-processing in News Headlines
All news headlines were pre-processed before being classified as a positive or negative news headline: 
- Step 1: Transform all news headlines into lower-case headlines. 
- Step 2: Remove all punctuations in the headlines. 
- Step 3: Remove words that do not add information to the sentences (stop words). 
The processed news headlines were then feed to a pre-trained sentiment analysis model and were classified to have positive or negative sentiments. 

## References: 
* Bishop, C. (2006). Pattern Recognition and Machine Learning. Springer.
* Chen, Z., & Brown, E. (2013, June 13). State space model. Scholarpedia. Retrieved December 17, 2021, from http://www.scholarpedia.org/article/State_space_model
* Meyler, A., Kenny, G., & Quinn, T. (1998). Forecasting irish inflation using ARIMA models. Munich Personal RePEc Archive, 1-48. https://mpra.ub.uni-muenchen.de/11359/1/cbi_3RT98_inflationarima.pdf
* Shumway, R., & Stoffer, D. (2000). Time Series Analysis and Its Applications. Springer.


