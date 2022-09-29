# ARIMA
## (Auto Regressive Integrated Moving Average)

ARIMA, is actually a class of models that explains a given time series based on its own past values, that is, its own lags(previous values) and the lagged forecast errors, so that equation can be used to forecast values. <br>

There are many kinds of dataforms, be it seasonal, non-seasonal arima model can fit in any zone. <br>

Any non-seasonal time series that exibits patterns and is not a random white noise can be modeled with arima model. <br>

ARIMA model is characterized by 3 terms <b> p, q, d </b> <br>

Where <br>

p is the order of AR (auto regressive) term <br>
q is the order of the MA (moving average) term <br>
d is the number of differencing required to make time series stationary <br>

<b><i>note - if you observe a seasonal pattern then you need to add seasonal terms and it becomes SARIMA, short or "Seasonal ARIMA"</i></b> <br> 

## What is p, d and q in ARIMA model

First let us understand the fundamentals that bought the idea of ARIMA model.
### AR (Auto Regressive)
AR in ARIMA means it is a linear regression model that uses its own lags as predictors. Linear regression models as you know works best when the predictors are not correlated and are independent with each other. <br>

<i> So what makes series stationary? </i> <br>
The most common way is to difference it. That is, substracting previous value from the current value. differencing may depend on complexity of the series. <br>
The value of d, therefore, is the minimum number of differencing needed to make the series stationary. If the time series is already stationary, then d = 0 <br>
Now what is "p" and "q" means ? <br>
"p" is the order of AR. It refers to the number of lags of Y to be used as predictors, and "q" is the order of "Moving average (MA)", which refers to the number of lagged forecast errors that should go into the ARIMA model. <br>





