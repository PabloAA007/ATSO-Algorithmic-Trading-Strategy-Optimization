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
  
# Executive Summary 
- This project explores the use cases of Natural Language Processing (NLP) and Financial Technical analysis tools within the Financial Technology industry to produce a forecast/predictions of future stock price trends. 
- The outcome was achieved through the implementation of multiple tools within the overall categories listed above, for example: Natural Language Processing (NLP) tools like the SentimentIntensityAnalyzer, Machine Learning (ML)/forecasting models such as Prophet Model & Linear Regression models. The project also utilizes API tools such as the News API & Yahoo Finance API to retrieve the data necessary for analysis, as well as python to preprocess and clean up the data that made the analysis possible.  
- Through the use of fundamental, technical, & NLP analysis techniques we are looking to reveal and predict potential future market movements/trends based on qualitative and quantitative data related to a particular industry or individual stock of a company itself.

# Project Goals
The goal of the project was to develop a comprehensive set of code to provide the ability to predict the future stock price trends of any stock we would like to examine this use case with. The code will provide an assessment on the stock's future price trends based on the combination of the results returned from the two methods that have been used, that being sentiment analysis and technical analysis. By providing an overall assessment based on both sentiment analysis and the technical analysis in combination, our projects output is able to get a more accurate prediction of the future stock price trends by looking at both the quantitative aspect of the market, i.e. investor sentiment in the market around a particular stock, and the quantitative side of things as well, i.e. historical stock price data. 

# Scope of analysis:
To achieve the end goal relating to the sentiment analysis portion of the project, we needed to see whether the news articles we were running through our code would be ultimately classified as having positive, negative and neutral sentiment around them. To collect the data for the csv file that is created and used to filter for the stock of our choice, Apple, we utilized an API called News API, which gave us the ability to filter for a group of stocks and the quantitative data type of our choice for that stock, allowing us to collect and return news articles over time related to the stocks we choose. Once the API requests had been made for english news articles on the stocks, the data was run through a forloop, collected and stored in a list. Then we instantiated our SentinmentIntensityAnalyzer and created a forloop that would run through the list of news articles in our stock list, analyze and transform the qualitative data into a quantitative sentiment score. We were then able to filter the data into a csv file containing the sentiment scores of news surrounding Apple's business activity. Once the article data points had been assigned a sentiment score by the NLP model, we counted the number of positive, neutral, and negative scores to give us an overall result of the breakdown of the scores.

The technical analysis portion of the project involved using a couple different machine learning models to forecast and make predictions about the future stock price trends of Apple in particular. The first model we used was the linear regression model to produce a prediction of where the stock price would move in the next 30 days. The data for this model was extracted from the Yahoo Finance API for the past 3 years of historical stock price data on Apple. The data was turned into a data frame, cleaned and formatted so it was ready for analysis. Data was split into a training and testing set and then ran through and fitted to the model to give us our future price forecast/predictions. Our results from this model indicated that the future price trend of Apple for the next 30 days seems to be positive and on the incline. 

## Prophet_model
Time series forecasting using the Facebook Prophet library. It demonstrates how to load financial data, preprocess it, and use Prophet to make predictions. 

* Loading financial data (e.g., stock prices, economic indicators). <br>
* Preprocessing and cleaning the data (e.g., handling missing values, adjusting date formats). <br>
* Training a Prophet model to forecast future stock prices. <br>
* Visualizing the forecasted results using interactive plots. <br>

![image](https://github.com/PabloAA007/ATSO-Algorithmic-Trading-Strategy-Optimization/assets/125240804/63738534-9346-4261-8b13-92394d486979)

## Natural Language Processing
Natural Language Processing (NLP) techniques are applied to analyze the sentiment of financial news articles related to specific stocks.

Loading a dataset containing financial news articles and sentiment scores. <br>
Preprocessing the text data (e.g., lowercase, tokenization, stop-word removal). <br>
The Dataset was stored in a CSV file.

![image](https://github.com/PabloAA007/ATSO-Algorithmic-Trading-Strategy-Optimization/assets/125240804/ecef1d89-fa03-4d20-8e8c-93a0924b5d1e)

Splitting the data into training and testing sets. <br>
Vectorizing the text data using TF-IDF (Term Frequency-Inverse Document Frequency). <br>
Training a sentiment analysis model (e.g., Naive Bayes, Random Forest) to predict sentiment scores. <br>
Evaluating the model's performance using Mean Squared Error. <br>
Visualizing the model's predictions and actual sentiment scores. <br>

![image](https://github.com/PabloAA007/ATSO-Algorithmic-Trading-Strategy-Optimization/assets/125240804/f2d6ed9c-a309-4be0-9474-7b87cc4f5b6f)

## Static_webscraper.ipynb
Create a static web scraper to extract content from financial news articles on Yahoo Finance. 

Using the requests library to make an HTTP request to a specific URL. <br>
Parsing the HTML content of the page using BeautifulSoup. <br>
Extracting the article content from the HTML, specifically focusing on the main body of the article. <br>
Saving the extracted article content to a CSV file for further analysis. <br>

## Results

### Technical Analysis

As we can see from the AAPL share price from the start of the year, it is on a significant bull run. In the graph below displays 
the stability of this blue chip stock,  its not a surprise the linear regression model predicted a stable gradual growth over the course of the next 30 days.

![image](https://github.com/PabloAA007/ATSO-Algorithmic-Trading-Strategy-Optimization/assets/125240804/d0b9c143-45f5-4f85-acb1-45f43215957d)

Our linear regression for our sentimental analysis, tends to show a trend of positive correlation.  There are some outliers below the line, however, our model has too many points of predicting higher sentiment than what actually showed up.

Mean Squared Error: 0.057052474980422443

However, we did have a low MSE score.  Leaving us to believe this model was pretty good but not exceptionally strong. 

![image](https://github.com/PabloAA007/ATSO-Algorithmic-Trading-Strategy-Optimization/assets/125240804/6d14c95d-20a6-453d-b4fd-ef24a12b0754)

Graph 1 at the top shows the AAPL share price over the course of the last month.  Graph 2 is the daily percent change, as we can see they are perfectly correlated.  
Graph 3 takes the sentiment of different articles with AAPL in the title and creates the average daily sentiment.  As we can see, the plots are all scattered, as the sentiment points don't seem to have a true correlation to the above graphs.

![image](https://github.com/PabloAA007/ATSO-Algorithmic-Trading-Strategy-Optimization/assets/125240804/c55e23d6-51c1-43ae-b0ca-d2690819902f)

### Sentiment Analysis 

Here is a pie graph to depict what sentiment ranking the 100 articles we collected were. Apple has 4 times the amount of positive articles to negative.

This chart could potentially support the prophet model  predictions for the bull trend.

![image](https://github.com/PabloAA007/ATSO-Algorithmic-Trading-Strategy-Optimization/assets/125240804/4dee9981-7e44-4cdd-a7f2-bbd72807e306)

## Conclusion

In conclusion, there is an upward trend in AAPL stock supported by our profit model.
The sentimental analysis was initially supposed to support the technical analysis as a factor to predict the stock trend and price. Instead, it was utilized as a comparison to verify the technical analysis outcome. 

## Next Step

Include other sources to extract NLP data
* For example: Twitter API, pygooglenews, Reuters Corpus
* Web Scraping

Alter the dataset to include more content
* Have access to a larger pull request option (paid API)
* Utilize larger content (entire article content instead of descriptions)
* Expand Dataset timeline (greater than 30 days)

Utilize more NLTK libraries to filter the dataset
* Tokenization
* Stemming

Utilize NLP and other machine learning model outputs to predict stock prices and trends
* Streamlit Application


