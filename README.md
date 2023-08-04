# The NLP Stock Prophet: Forecasting Words into Wealth

![Words into Wealth](https://realpython.com/cdn-cgi/image/width=960,format=auto/https://files.realpython.com/media/NLP-for-Beginners-Pythons-Natural-Language-Toolkit-NLTK_Watermarked.16a787c1e9c6.jpg)

**Team Members:** <br>
Athura Thavathasan <br>
Brandon Petrie <br>
Harshitha Katta <br>
Nicholas Gracan <br>
Pablo Aray Acevedo <br>

Presentation: https://docs.google.com/presentation/d/1bbsZ5Q9QETytBUTxkvsNPNWXn1ky3E_qByOCSHYsecM/edit?usp=sharing

*Presentation Aug 03rd, 2023*

## Overview
The project focuses on building an algorithmic trading system to predict the future trends of any given stock. Focusing on Apple Inc. (AAPL) stock prices using the Prophet library, through a combination of sentiment analysis, time series forecasting, and text analysis we tried to understand potential market movements and make informed investment decisions. By analyzing historical AAPL stock price data, we aim to generate forecasts for the next 30 days, providing valuable insights into possible future price movements. Additionally, we utilized the Natural Language Toolkit (NLTK) for text analysis to extract meaningful information from news articles. Combining time series forecasting and text analysis will give us valuable insights into AAPL stock price trends and market sentiment from news articles, enhancing our ability to make data-driven investment decisions. <br>

# Libraries 
## Import Libraries

- Pandas: (`pip install pandas`)
- NumPy: (`pip install numpy`)
- Prophet library: (`pip install prophet`)
- scikit-learn: pip install scikit-learn
- Holoviews: (`pip install holoviews`)
- Matplotlib: (`pip install matplotlib`)
- Requests: (`pip install requests`)
- Hvplot: (`pip install hvplot`)
- Natural Language ToolKit: (`pip install nltk`)

# Project Goals
The goal of the project was to develop a comprehensive set of code to provide the ability to predict the future stock price trends of any stock we would like to examine this use case with. The code will provide an assessment on the stock's future price trends based on the combination of the results returned from the two methods that have been used, that being sentiment analysis and technical analysis. By providing an overall assessment based on both sentiment analysis and the technical analysis in combination, our projects output is able to get a more accurate prediction of the future stock price trends by looking at both the quantitative aspect of the market, i.e. investor sentiment in the market around a particular stock, and the quantitative side of things as well, i.e. historical stock price data. 

Scope of analysis:
To achieve the end goal relating to the sentiment analysis portion of the project, we needed to see whether the news articles we were running through our code would be ultimately classified as having positive, negative and neutral sentiment around them. To collect the data for the csv file that is created and used to filter for the stock of our choice, Apple, we utilized an API called News API, which gave us the ability to filter for a group of stocks and the quantitative data type of our choice for that stock, allowing us to collect and return news articles over time related to the stocks we choose. Once the API requests had been made for english news articles on the stocks, the data was run through a forloop, collected and stored in a list. Then we instantiated our SentinmentIntensityAnalyzer and created a forloop that would run through the list of news articles in our stock list, analyze and transform the qualitative data into a quantitative sentiment score. We were then able to filter the data into a csv file containing the sentiment scores of news surrounding Apple. 

## Prophet_model
Time series forecasting using the Facebook Prophet library. It demonstrates how to load financial data, preprocess it, and use Prophet to make predictions. 

Loading financial data (e.g., stock prices, economic indicators). <br>
Preprocessing and cleaning the data (e.g., handling missing values, adjusting date formats). <br>
Training a Prophet model to forecast future stock prices. <br>
Visualizing the forecasted results using interactive plots. <br>

## Natural Language Processing
Natural Language Processing (NLP) techniques are applied to analyze the sentiment of financial news articles related to specific stocks.

Loading a dataset containing financial news articles and sentiment scores. <br>
Preprocessing the text data (e.g., lowercase, tokenization, stop-word removal). <br>
Splitting the data into training and testing sets. <br>
Vectorizing the text data using TF-IDF (Term Frequency-Inverse Document Frequency). <br>
Training a sentiment analysis model (e.g., Naive Bayes, Random Forest) to predict sentiment scores. <br>
Evaluating the model's performance using Mean Squared Error. <br>
Visualizing the model's predictions and actual sentiment scores. <br>

## Static_webscraper.ipynb
Create a static web scraper to extract content from financial news articles on Yahoo Finance. 

Using the requests library to make an HTTP request to a specific URL. <br>
Parsing the HTML content of the page using BeautifulSoup. <br>
Extracting the article content from the HTML, specifically focusing on the main body of the article. <br>
Saving the extracted article content to a CSV file for further analysis. <br>

## Conclusion
