# Time-Series-Analysis

# Introduction to Time Series Analysis

**What is Time Series ?**
- A time series is a sequence of data being recorded at a specific time intervals.

**Where the Time Series is used ?**
- Statistics
- Econometrics
- Mathematical Finance
- Weather Forecasting
- Earthquake Prediction
- Stock Market Prediction

**What is Time Series Analysis ?**
- Analyzing the data to find pattern.

**What is Forecasting ?**
- Forecasting is the process of making predictions of the future based on past and present data and most commonly by analysis of trends.

**Factors for determining Forecasting**
- The amount of data.
- The clarity of the pattern.
- Does the forecast affect the time series ?.

**Time Series can not use if**
- The data have constant or same previous value.
- Non stationary data.

**Types of Time Series**
- **Univariate Time Series** : Only one variable is varying over time. For example, data collected from a sensor measuring the temperature of a room every second. Therefore, each second, you will only have a one-dimensional value, which is the temperature.
- **Multivariate Time Series** : Multiple variables are varying over time. For example, a tri-axial accelerometer. There are three accelerations, one for each axis (x,y,z) and they vary simultaneously over time.

**Record of TS frequency**
- Hourly
- Daily(24 hrs)
- Weekly
- Monthly
- Quarterly
- Yearly

**What is Cross Sectional Data ?**
- A type of data collected by observing many subjects at the one point or period of time.

**Component of Time Series**
- Level: The average value in Time Series.
- Trend: Increase or decrease of trend in the long period of time say 5 to 10 years.
- Seasonality: Upward or Downward due to season in the short period of time say 1 year or 2 years or 3 years.
- Noise: The random variation in Time Series.
- Cyclicity: Upward or Downward due to circumstances like inflation or recession.
- Irregularity: Upward or Downward due to natural calamities like earthquake, flood, war.

**What is Decomposition ?**
- Decomposition is the deconstruction of the series data into its various components: trend, cycle, noise, and seasonality when those exist. 
- Two different types of classic decomposition include multiplicative and additive decomposition.

**What is Multiplicative Time Series ?**
- When the fluctuations in the time series increase over time and is dependent on the level of the series.
- Multiplicative Model: Time series  = t (trend) * s (seasonality) * n (noise)

![image](https://user-images.githubusercontent.com/77838416/111447577-9488b080-8733-11eb-944d-8fbd4d203f37.png)

**What is Additive Time Series ?**
- An additive model is when the fluctuations in the time series stay constant over time.
- Additive Model: Time series  = t (trend) + s (seasonality) + n (noise)

![image](https://user-images.githubusercontent.com/77838416/111447718-b5e99c80-8733-11eb-9aa0-8c8617582fa5.png)

**Assumption of Time Series**
- Linear Regression has an assumption that the value is dependent of its own previous values.
- Today's value depends on yesterday's value.
- Today's time denoted as Yt.
- Yesterday's time denoted as Yt-1.

**What is Lag ?**
- In time series, lag is a time period gap between the period.
- Lags are where results from one time period affect following periods.
- Example: Stock Price {110,112,118,125,131}
- Lag 1 of Stock Price {112,118,125,131}
- Lag 2 of Stock Price {118,125,131}
- Lag 3 of Stock Price {125,131}

**What is White Noise ?**
- It is a puraly random in nature i.e. We can not identify any pattern like trend, seasonlality, Cyclacity, irregularity.
- Each observation is uncorrelated with other observations in the sequence.

**Condictions for Identify the White Noise**
- E(Yt) = Constant Mean
- Var(Yt) = Constant Variance
- Auto Covariance = 0 There is no correlation

**Why it is required to find white noise ?**
- Because if the observations have white noise are uncorrelated and independent hence it is very hard to predict.

# Methods of Time Series Analysis

# Simple Moving Average

**What is Simple Moving Average ?**
- Simple Moving Average is calculated by adding observations for last K time periods in time series and divide that sum by K.
- Formula: Ft+1=(Yt+Yt-1+Yt-2+Yt-3+……Yt-K+1)/K.
- Equal weightage is given to all observations in last K periods.
- Smaller the value of K, the greater weight is given to each period.
- Short term simple moving average responds quickly to changes in the time series.
- Greater the value of K, the smaller weight is given to each period.
- Long term simple moving average are comparably slow to react.
- Drawback: Exact same weight to the selected period, What happened yesterday have a different.

**What is Weighted Moving Average ?**
- A weight is assigned to each term to be averaged. 
- These particular weights signifies the relative importance of each term on the average. 
- The sum of all the associated weights should be equal to 1.
- Formula: Ft+1=(Wt*Yt+Wt-1*Yt-1+Wt-2*Yt-2+Wt-3*Yt-3+……Wt-k+1*Yt-K+1)
- Wt-Weight assigned to Sales in time period t
- Yt- Actual Sales in time period t
- Higher the weight associated with the recent terms, quicker the response to the change in time series happen to the forecasted output.

# Exponential Smoothing

**What is Exponential Smoothing ?**
- Exponential smoothing is simply an adjustment technique which takes the previous period's forecast, and adjusts it up or down based on what actually occurred in that period
- Recent observations are given relatively more weight in forecasting than the older observations.
- Exponentially decreasing weights as the observation get older.
- Removing much of the “noise”.

**What is Single Exponential Smoothing ?**
- It is a Simple Exponential Smoothing. 
- It is used when data does not have trend and seasonality.
- It is require single parameter called Alpha α.

**What is Apha ? or What is a Hyperparameters of SES ?**
- It is a smoothing factor or smoothing coefficient.
- This parameter controls the rate at which the influence of the observations at prior time steps decay(loss) exponentially.
- Alpha lie in 0 and 1 so that a part of difference between previous and predicted can be updated.
- If Alpha is close to 1 then it has less smoothing effect and give greater weight to the recent changes in data(pays attention mainly to the most recent past observations).
- If Alpha is close to 0 then it has greater smoothing effect and less responsive to recent changes in data(More of the history is taken into account ).
- Formula: Predictive Value + Alpha(Actual Value - Predictive Value)

**What is Double Exponential Smoothing ?**
- Double Exponential Smoothing is an extension to Exponential Smoothing that explicitly adds support for trends in the univariate time series. 
- It is also called Holt ES.
- It has a two parameters, Alpha & Beta.
- Alpha use for data smoothing parameter and Beta use for trend Smoothing Parameter.
- Beta control the decay of the influence of the change in trend.

**What is Triple Exponential Smoothing**
- Triple Exponential Smoothing is an extension of Exponential Smoothing that explicitly adds support for seasonality to the univariate time series. 
- It is also called Holt Winters ES. 
- It require three parameter Alpha α , Beta β, Gamma y & Phi.
- Alpha use for data smoothing parameter (Controls Levels).
- Beta use for trend smoothing parameter(Controls Trend component).
- Gamma use for seasonal smothing parameter(Control Seasonal component.

# Stationarity or Stationary Time Series

**What is Stationarity ?**
- Stationarity is the property of exhibiting constant statistical properties (mean, variance, autocorrelation, etc.). 
- If the mean of a time-series increases over time, then it’s not stationary.
- Mean, Variance and Covariance remain unchanged. 
- There should not be upward or down wards.

**Types of Stationarity**
- **Strictly Stationarity**: 
  - A random process whose joint distribution doesn't change over time. 
  - If the joint distribution of the time series process remain same (Unchange) overtime  it is called strict stationarity.
- **Weakly Stationarity**: 
  - Mean and the variance are not constant through time. 
  - They keep changing with time. 
  - It is also known as covariance stationarity.

#Auto Regressive Model

**What is Auto Regressive Model ?**
- It is an AR model predicts future behavior based on past behavior.
- It is an example of stochastic process(Stochastic - having a random probability distribution or pattern that may be analysed statistically but may not be predicted precisely).
- Yt depends only on its own past values AR(p) in which p is a Past Value
- An AR(p) model is an autoregressive model where specific lagged values of yt are used as predictor variables. 
- The value for “p” is called the order.
- Formula: Yt = B0 + B1*Yt-1 + B2*Yt-2 +…..Bp*Yt-p + Et

**What is Past Values ?**
- Past Values yt-1, yt-2, yt-3, Et-……………..So on.

**What is Auto ?**
- When the value from a time series is regressed on previous values from that same time series 
