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


