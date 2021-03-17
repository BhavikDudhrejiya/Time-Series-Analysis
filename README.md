# Time-Series-Analysis

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
- Because if the observations are in white noise are uncorrelated and independent and hence it is very hard to predict.

