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
<br>
A pure Auto regressive model is when Yt depends only on its own lags. that is, Yt is a function of the <b>"lags of Yt"</b> <br>

Yt = a + b1Yt-1 + b2Yt-2 + ... + bnYt-n+ E1 <br>

where, Yt-1 is the lag1 of the series, b1 is the coefficient of lag1 that the model estimates and a is the intercept term, also estimated by model. <br>

Likewise, a pure Moving Average is one where Yt depends only on the lagged forecast errors. <br>
Yt = a + E1 + b1Et-1 + b2Et-2 + bnEt-n <br>
where the error terms are the errors of the autoregressie model of the respective lags. The errors Et and Et-1 are the errors from the following equations: <br>

Yt = b1Yt-1 + b2Yt-2 + ... + b0Y0 + Et <br>
Yt-1 = b1Yt-2 + b2Yt-3+ ... + b0Y0 + Et-1 <br>

So final arima model will look like, <br>

An ARIMA model is one where the time series was differenced at least once to make it stationary and you can combine the AR and the MA terms, SO the equation becomes <br>

<b>Predicted Yt = Constant + Linear combination Lags of Y (upto p lags) + Linear Combination of Lagged forecast errors (upto q lags) </b> <br>

The major objective is to find the value of p ,q and d. <br>

### Finding the value of d
The main purpose of d is to make time series stationary. But we need to be careful that we dont over do it because over differencing may look stationary but its will affect the model parameters. <br>
The right order of differencing is the minimum differencing required to get a near-stationary series which roams around a defined mean and the <b> ACF</b> plot reaches to zero fairly quick. <br>

If the autocorrelations are positive for many number of lags say 10 or more, then the series needs further differencing. On the other hand, id the lag 1 autocorrelation itself is too negative, then the series is probably <b>over-differencing</b><br>

In a event you cannot really decide between two orders of differencing, then go with the order that gives the least standard deviation in the differenced series. <br>

To check series to be stationary we use <b>Augmented Dickey Fuller test (adfuller ())</b> from the stats model package. <br>

<b>P-value threshold = 0.05</b>
if P-value is smaller than 0.05 then it is considered to have a stationary series. else, we need further differencing.







