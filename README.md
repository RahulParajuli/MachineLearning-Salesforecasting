# MachineLearning-Salesforecasting
Different algorithms for forecasting sales and finding the predictive value of ongoing trends and also predict the future forecasting

# TIME SERIES

Time series is the sequence where a metric is recorded over regular interval of time. <br>
Depending on the frequency, time series can be yearly, quaterly, monthly, weekly, daily, hour-minute-second etc. <br>
Some major problem solved by using time series analysis/forecasting are, <br>
- Annual budgetting. <br>
- Quarterly expenses calculation <br>
- Montly Air traffic <br>
- Weekly sales forecasting <br>
- Daily weather updates <br>
- Hourly stock price prediction <br>
- Minute basis call logs in call center <br>
- In second web traffic analysis <br>

Forecasting can add tremendous amount of commercial values. In most manufacturing companies, it drives the fundamental business planning, procurement and production activities. It is very important to have higher precision of accuracy in forecasting future sales such that it is a basis of businesses to increase or decrease production. <br>

Time series analysis is further divided into two types, <br>
- Univariate Time Series Forecasting.
- Multivariate Time Series Forecasting.

## Models to work as a sales forecaster
- ARIMA (AutoRegressive Integrated Moving Average)
- fbprophet (developed by facebook as a open source project)
## ARIMA [link](https://github.com/RahulParajuli/MachineLearning-Salesforecasting/blob/3c85ca47b15d46b0c6133454a8672cf506c79e36/ARIMA)
An autoregressive integrated moving average, or ARIMA, is a statistical analysis model that uses time series data to either better understand the data set or to predict future trends.<br>
A statistical model is autoregressive if it predicts future values based on past values. For example, an ARIMA model might seek to predict a stock's future prices based on its past performance or forecast a company's earnings based on past periods.

## fbprophet [link](https://github.com/RahulParajuli/MachineLearning-Salesforecasting/blob/3c85ca47b15d46b0c6133454a8672cf506c79e36/fbprophet)
Prophet is a method for predicting time series data that uses an additive model to suit non-linear trends with seasonality that occurs annually, monthly, daily, and on weekends as well as during holidays. Strongly seasonal time series and multiple seasons of historical data are ideal for it. Prophet typically manages outliers well and is robust to missing data and changes in the trend.
