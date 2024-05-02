# bitcoinmodel
Created a bitcoin price prediction model based on data from 2018 Jan - 2024 April

As the price and talks of cryptocurrencies have increased, I have decided to create a project that is centred around creating a predictive model that can accurately predict the future price of Bitcoin based on historical data. This project aims to address a real world problem that may be applicable in the financial sector, which is creating algorithms to help statistically gauge whether one should invest or not. Additionally, we will also create a model to predict the price of another altcoin, and then look into whether we can combine the two models to determine how the price of Bitcoin may influence the price of an altcoin. This is due to the fact that Bitcoin typically influences the market, and it is a common tendency for an altcoin to rise in price, if the price of BTC is increasing. All data used for creating this predictive model will be taken from Yahoo Finance, and the applicable links to the data will be under the “Retrieving Data”.


### **Structured Approach:**

**Bitcoin Price Prediction:**
Create a primary model that will leverage historical price data of Bitcoin to predict the future prices. The model will use the historical open, high, low, close, and volume data to predict future prices.
The model will be evaluated on its ability to generalise unseen data which in this situation will likely include predicting the price of Bitcoin for the months of January 2024 to April 2024 ~ This is subject to change as seen below in the test sets.

**Altcoin Price Prediction:**
Create a secondary model that will leverage the same historical price data for a specific altcoin, to predict future prices.
The model will be evaluated similar to the first model.

**Combined Model:**
Determine whether we can combine the Bitcoin and altcoin models to create an enhanced predictive model. The goal of this model is to determine how Bitcoin’s market behaviour could impact the broader market.


We will use a LSTM model, as it is specifically designed to work with sequences of data that are spread across many time periods. LSTM models are able to model financial data on a greater scale as they are able to remember data over greater time periods without generalising or losing the general focus of the data. Additionally, LSTM models can handle historic price data well, and can determine patterns like peaks, and trends from sequential data, making it an ideal approach for predicting future prices with a high degree of accuracy.


### **Retrieving the Data:**

As with all predictive models, there must be a robust data set which we can preprocess to have it ready for developing a model. The dataset used for this project has been sourced from Yahoo Finance, which is a reputable financial news and data provider. 

**Data Source:**
Yahoo Finance URL for Bitcoin Data: Yahoo Finance - BTC-USD

Yahoo Finance URL for Chainlink Data: Yahoo Finance - LINK-USD

Data Coverage:  This webpage provides options to download the historical data for various time frames, which in this case we will be working with daily data from January 1st 2018, to April 23rd 2024. 

Available Features: The dataset includes the following features:

Open - The price of Bitcoin at the beginning of the day

High - The highest price of Bitcoin during the day

Low - The lowest price of Bitcoin during the day

Close - The price of Bitcoin at the end of the day

Adjusted Close - The adjusted closing price which considered any corporate actions. Approximately the same as the closing.

Volume - The total volume of Bitcoin traded during the day.

