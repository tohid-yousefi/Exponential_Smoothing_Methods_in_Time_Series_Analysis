# Exponential Smoothing Methods in Time Series Analysis
In this section, we will examine the Exponential Smoothing Methods in time series analysis.

<hr />

📌 Exponential smoothing is a time series forecasting method for univariate data that can be extended to support data with a systematic trend or seasonal component.

**Types of Exponential Smoothing:**

  1. **Single Exponential Smoothing**
    
  📌 Single Exponential Smoothing, SES for short, also called Simple Exponential Smoothing, is a time series forecasting method for univariate data without a trend or seasonality.

  📌 It requires a single parameter, called alpha (a), also called the smoothing factor or smoothing coefficient.

  📌 This parameter controls the rate at which the influence of the observations at prior time steps decay exponentially. Alpha is often set to a value between 0 and 1. Large values mean that the model pays attention mainly to the most recent past observations, whereas smaller values mean more of the history is taken into account when making a prediction.

  2. **Double Exponential Smoothing**
  
  📌 Double Exponential Smoothing is an extension to Exponential Smoothing that explicitly adds support for trends in the univariate time series.

  📌 In addition to the alpha parameter for controlling smoothing factor for the level, an additional smoothing factor is added to control the decay of the influence of the change in trend called beta (b).

  📌 The method supports trends that change in different ways: an additive and a multiplicative, depending on whether the trend is linear or exponential respectively.

  📌 Double Exponential Smoothing with an additive trend is classically referred to as Holt’s linear trend model, named for the developer of the method Charles Holt.

* **Additive Trend**: Double Exponential Smoothing with a linear trend.
* **Multiplicative Trend**: Double Exponential Smoothing with an exponential trend.

  📌 For longer range (multi-step) forecasts, the trend may continue on unrealistically. As such, it can be useful to dampen the trend over time.

3. **Triple Exponential Smoothing**

  📌 Triple Exponential Smoothing is an extension of Exponential Smoothing that explicitly adds support for seasonality to the univariate time series.

  📌 This method is sometimes called Holt-Winters Exponential Smoothing, named for two contributors to the method: Charles Holt and Peter Winters.

  📌 In addition to the alpha and beta smoothing factors, a new parameter is added called gamma (g) that controls the influence on the seasonal component.

  📌 As with the trend, the seasonality may be modeled as either an additive or multiplicative process for a linear or exponential change in the seasonality.

* **Additive Seasonality**: Triple Exponential Smoothing with a linear seasonality.
* **Multiplicative Seasonality**: Triple Exponential Smoothing with an exponential seasonality.

  📌 Triple exponential smoothing is the most advanced variation of exponential smoothing and through configuration, it can also develop double and single exponential smoothing models.


# Business Problem

📌 Our aim here is to estimate the amount of air pollution (co2) one month later.

# Dataset Story

📌 The carbon dioxide record from Mauna Loa Observatory, known as the “Keeling Curve,” is the world’s longest unbroken record of atmospheric carbon dioxide concentrations. Scientists make atmospheric measurements in remote locations to sample air that is representative of a large volume of Earth’s atmosphere and relatively free from local influences.

Atmospheric CO2 from Continuous Air Samples at Mauna Loa Observatory, Hawaii, U.S.A.
Period of Record: March 1958 - December 2001
