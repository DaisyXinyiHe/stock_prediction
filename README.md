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

```math
a^2+b^2=c^2

Stock Price Change Percentage = (Closing Price<sub>t</sub> - Closing Price<sub>t-1</sub> )Closing Price<sub>t-1</sub> 100
```

calculate the percentage of change in closing price as stock return:
$$
Stock Price Change Percentage = (Closing Pricet - Closing Pricet-1)Closing Pricet-1*100 .
$$

