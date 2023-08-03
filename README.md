# The NLP Stock Prophet: Forecasting Words into Wealth

![Words into Wealth](https://realpython.com/cdn-cgi/image/width=960,format=auto/https://files.realpython.com/media/NLP-for-Beginners-Pythons-Natural-Language-Toolkit-NLTK_Watermarked.16a787c1e9c6.jpg)

**Team Members:** <br>
Athura Thavathasan <br>
Brandon Petrie <br>
Harshitha Katta <br>
Nicholas Gracan <br>
Pablo Acevedo <br>

*Presentation Aug 03rd, 2023*

## Overview
The project focuses on building an algorithmic trading system to predict the future trends of any given stock, Apple Inc. (AAPL) stock prices using the Prophet library. Through a combination of sentiment analysis, time series forecasting, and text analysis to understand potential market movements and make informed investment decisions. By analyzing historical AAPL stock price data, we aim to generate forecasts for the next 36 months, providing valuable insights into possible future price movements. Additionally, we will utilize the Natural Language Toolkit (NLTK) for text analysis to extract meaningful information from news articles. Combining both time series forecasting and text analysis will enable us to gain valuable insights into AAPL stock price trends and market sentiment from news articles, enhancing our ability to make data-driven investment decisions. <br>

# Libraries 
## Import Libraries

- Prophet library (`pip install prophet`)
- Holoviews (`pip install holoviews`)
- Hvplot (`pip install hvplot`)
- Natural Language ToolKit(`pip install nltk`)

# Project Goals
The goal of the project was to develop a comprehensive set of code to provide the ability to predict the future stock price trends of any stock we would like to examine this use case with. The code will provide an assessment on the stock's future price trends based on the combination of the results returned from the two methods that have been used, that being sentiment analysis and technical analysis. By providing an overall assessment based on both sentiment analysis and the technical analysis in combination, our projects output is able to get a more accurate prediction of the future stock price trends by looking at both the quantitative aspect of the market, i.e. investor sentiment in the market around a particular stock, and the quantitative side of things as well, i.e. historical stock price data. 

Scope of analysis:
To achieve the end goal relating to the sentiment analysis portion of the project, we needed to see whether the news articles we were running through our code would be ultimately classified as having positive, negative and neutral sentiment around them. To collect the data for the csv file that is created and used to filter for the stock of our choice, Apple, we utilized an API called News API, which gave us the ability to filter for a group of stocks and the quantitative data type of our choice for that stock, allowing us to collect and return news articles over time related to the stocks we choose. Once the API requests had been made for english news articles on the stocks, the data was run through a forloop, collected and stored in a list. Then we instantiated our SentinmentIntensityAnalyzer and created a forloop that would run through the list of news articles in our stock list, analyze and transform the qualitative data into a quantitative sentiment score. We were then able to filter the data into a csv file containing the sentiment scores of news surrounding Apple. 

