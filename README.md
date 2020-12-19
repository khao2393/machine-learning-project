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

In addition to Random Forests, we used neural networks machine learning models -- 
LSTM-RNN (recurring neural network) and LSTM-CNN (convolutional neural networking) to predict the future stock prize.
We used the Open prize as the feature column and the closing prize as the target column.

## LSTM-RNN and LSTM-CNN

While we were able to create several models that effectively forecast a stock price, it wasn't accurate enough to be used for day trading because of too much of a time lag 
between actual and predicted closing prices. 

However, they seem to be helpful predicting/understanding long term trends within the stock.

## Trade Signal Backtesting

### How did we develop our trade signals?

We as a team had to agree on 2 key decisions when developing our trade signal: what technical tool would be most appropriate to track the movement of stocks, and what consitiutes a buy/sell decision. We as a team decided to use the 50 day moving average as our technical indicator to help us determine our buy and sell signals. From there we decided that when the price of a stock was below its 50 day moving average that would trigger a buy decision from out model and when the stock price was above the 50 day moving average that would trigger a sell decision. 

### Implementation of our Trade signals 

The results of out testing was 98 signals to either enter or exit MSFT. The signals seemed to be clustered fairly close together.

### Results of Trade Signals with Backtesting

Using our trade signals we simulated an investor with 100,000 dollars who wants to invest in our technical trade signal. Through calculation we determined that the annual return of the technical signal would be 4.3651% annually. The cumulative return of the portfolio was 4.05479 which would mean you would have roughly 4x the amount of money at the end of your trading than you started with. The annual volatility of the portfolio was the most interesting aspect considering that you would have it annualized at 463.267. We generated a sharpe ratio that had negligible results meaning that it was neither good nor bad and didn't generate returns that were above the risk free return.

### Lessons from Technical Trade signals

*We learned that our 50 day moving average signal may not be the best to conduct a day trade strategy. In the future we look to see if using a 20 day moving average or even a 100 day moving average would allow us to have better returns and potentially get better returns based on further holding periods. 
*The amount of volatility for the amount of returns raised the question for us, is it worth taking a day trade approach or should we just implement a long term hold strategy where we buy and then hold MSFT for x amount of years. 
*Did we choose the correct stock to impliment a day trading strategy? It seems that MSFT was low volatility stock for many of the years of data we used which would be inopportune for a volatility based day trade strategy.
*Machine Learning can help us with day trade strategies in several ways:
    *Help predict stock prices
    *Understand Price momentum
    *Optimize our model to create better returns in the long term
## Final Remarks

During this project we worked to combine Machine learning with Technical analysis to create a model that could accurately predict stock prices and provide a tool that could generate greater returns for investors. Although there is a lot to be done in the world of Machine learning and stock predictions we did learn that Machine learning did a better job at predicting long term trends within the stock and the broad based market. We used technical analysis to generate a trade signal based on the crossing of the 50 day moving average and MSFT's stock price which would give us buy/sell signals. Although we were unable to integrate our 2 models into one cohesive model that predicts future prices we as a group are optimistic that the progress of machine learning will one day find a breakthrough and strategies will be built around it. 
