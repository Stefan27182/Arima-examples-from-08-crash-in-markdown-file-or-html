# Arima models, forecasts, and graphs
#### Stefan Skinner
#### 08/Nov/2022
###### [Data from Yahoo Finance](/https://finance.yahoo.com/)
***

#### The non-auto Arima models in this markdown file were arrived at, in part, 
#### by utilizing the following functions:
    01)  isSeasonal(full_ts, test = "fried")

    02)  adf.test(full_ts, alternative = c("stationary")) 

    03)  plot(decompose(full_ts))

    04)  ndiffs(full_ts)

    05)  diff(full_ts, lag = *)

    06)  adf.test(dif_ts)

    07)  urdfTest(dif_ts)

    08)  acf(dif_ts) #for zoomed view

    09)  pacf(dif_ts) #for zoomed view

    10)  plot(decompose(dif_ts))

    11   plot(df_ts, main = "", xlab = "", ylab = "")
   
    12)  lines(fitted(df_forecast), col="")

    13   checkresiduals(df_forecast)

***

#### Crude Oil
#### The auto arima summary in the image below is very basic; the next one below will be more modified i.e. contain "approximation" and "stepwise" equal false, will get only marginally better results, and will take much more time to process than the basic quick style shown initially.
![](Scores/Crude/Crude_AIC's.png)

![](Scores/Crude/Crude_auto_arima_long.png)

***

###### Crude Oil - Fitted Models
###### not auto
![](Models/Crude/Crude_Oil_w_Arima_model_[010][111]_blue_overlay.png)

###### auto.arima

![](Models/Crude/Crude_Oil_w_Arima_model_[010]_blue_overlay.png)

###### auto.arima

![](Models/Crude/Crude_Oil_w_Arima_model_[013][001]_blue_overlay.png)

***

##### Crude Oil - Forecasts
###### not auto

![](Forecasts/Crude/Crude_Oil_actual_01-06_w_Arima_[010][111]_[52]_07-09.png)

###### auto.arima

![](Forecasts/Crude/Crude_Oil_actual_01-06_w_Arima_[010]_07-09.png)

###### auto.arima

![](Forecasts/Crude/Crude_Oil_actual_01-06_w_Arima_[013][001]_[52]_07-09.png)

#### While the first model doesn't fit the data as well as the two that follow it (i.e. it is not overfitted), it still produces the best scores and the best looking graph out of the three.

***

##### Crude Oil - actual '01-'10
![](./actual_00_10/Crude_01_10_.png)

***

#### Gold
##### Gold - Model Summaries
![](./Scores/Gold/Gold_AICs_.png)

***

##### Gold - Fitted Models
###### auto.arima

![](Models/Gold/Gold_01-06_w_Arima_[010][001]_[52]_07-09_blue_overlay.png)

###### not auto

![](Models/Gold/Gold_01-06_w_Arima_[010][013]_[52]_07-09_blue_overlay.png)

***

##### Gold - Forecasts
###### auto.arima

![](Forecasts/Gold/Gold_01-06_w_Arima_[010][001]_[52]_07-09.png)

###### not auto

![](Forecasts/Gold/Gold_01-06_w_Arima_[010][013]_[52]_07-09.png)

***

##### Gold - actual '01-'10
![](actual_00_10/Gold_01_10_.png)

***

#### Silver
##### Silver - Model Summaries
![](Scores/Silver/Silver_AIC's_0.png)

#### Very close!

***

##### Silver - Fitted Models
###### not auto

![](Models/Silver/Silver__00_06__actual_w_ARIMA_[010]_[102]_blue_overlay.png)

###### auto.arima

![](Models/Silver/Silver_00_06_actual_w_ARIMA_[010][001]_blue_overlay.png)

***

##### Silver - Forecasts
###### not auto

![](./Forecasts/Silver/Silver__00_06__actual_w_Arima_[010][102]__07_09.png)

###### auto.arima

![](./Forecasts/Silver/Silver__00_06__actual_w_Arima_[010][001]__07_09.png)

***

##### Silver - actual '01-'10

![](./actual_00_10/Silver_00_10_.png)

***

### E-Mini
##### E-Mini - Model Summaries

![](Scores/E-Mini/E-Mini_AICs.png)

***

##### E-Mini - Fitted Models
###### auto.arima

![](Models/E-Mini/E-Mini_01-06_w_Arima_[010][100]_[52]_w_drift_blue_overlay.png)

######  not auto

![](Models/E-Mini/E-Mini_01-06_w_Arima_[010][011]_[52]_blue_overlay.png)

##### The addition of the seasonal component makes the fit look terrible (i.e. it is not overfitted to the data); never-the-less, it still produces the best scores and it adds an aesthetically satisfying wave to the graph. 

***

##### E-Mini - Forecasts
###### auto.arima

![](Forecasts/E-Mini/E-Mini_01-06_w_Arima_[010][100]_[52]_w_drift_07-09.png)

######  not auto

![](Forecasts/E-Mini/E-Mini_01-06_w_Arima_[010][011]_[52]_07-09.png)

***

![](actual_00_10/E-Mini_S&P_500_01_10_.png)



