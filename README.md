# Stock Predictions using Machine Learning
Ihar, Phil, Simon & Kevin


## Overview and Goals

* Use machine learning to help predict stock prices:

*Our team wanted to create a model that will accurately predict the stock price of MSFT using machine learning.* 

* Create Technical signals that will tell us when to buy and sell:

*Use trade signals to generate positive annual returns*

* Implement both strategies in tandem to create a strategy that allows for positive income

## Compiling the Data

* Which Data? 

*We decided to use 10 years worth of MSFT Data from 2012-12-01 to 2012-12-02 using Yahoo Finance. We used the 50 Day MA of the close price as our Entry/Exit Signals. If the close price was above the 50 day MA, this would be a Sell/Exit point. If the close price was below the 50 day MA, this wouuld be a Buy/Entry point. 1.0 signifies a Buy point, 0.0 signifies a Hold point and -1.0 signifies a Sell point.*

## Random Forests

*We decided to use Random Forests as one of our Machine Learning models for our project to predict entry/exit points. We used the y variable as the entry/exit signal and the rest of the columns as the x variable.*

* Results?

*It turns out the model was not sufficent enough to predict enough exit/entry points on our data set. Even though we scored an accuracy percentage of 93%, the model only predicted 2 sell points out of 23 sell points and 1 buy point out of 30 buy points. The reason the model scored a 93% accuracy score was because most of the data were hold points. There is a total of 687 hold points out of 741 points in the data set and the model predicted 684/687 hold points correctly.*

* What should we do next time?

*There weren't many exit/entry points in our data set. The Random Forests machine learning model did not have enough data to be trained on to predict buy/sell points. If we changed the 50 Day MA to a 20 Day MA, there might be more opportunties. Also, the first 5 years of MSFT from 2010-2015, the close price is relativley flat so there were not many changes to the close price. Most of the volatility came from the last 5 years.*

