## Introduction

Time series analysis focuses on data collected at successive intervals to uncover patterns and make forecasts. Unlike traditional regression models, which often miss temporal dynamics, ARIMA effectively captures these by incorporating autoregressive (AR), integrated (I), and moving average (MA) components to model correlations over time and improve prediction accuracy (Shumway & Stoffer, 2017; Statsmodels, n.d.).

## Objective
To analyze and forecast stock market feature values for Coursera using the ARIMA algorithm.

## Datasets

The <a href="https://finance.yahoo.com/quote/COUR/?guccounter=1" target="_blank">time series data</a> is from the stock market of Coursera and was gathered from Yahoo Finance, from 2021-03-31 to 2024-03-26. 

## Project execution

- Mitigate the presence of seasonality and trends using autocorrelation function (ACF) and partial autocorrelation function (PACF) plots.
  
- Find the optimal values for the ARIMA components: autoregressive (AR), integrated (I), and moving average (MA) models.

- Forecast future values using the optimal parameters of the ARIMA model.
  
## Results

- *Optimal ARIMA parameters*
  - Using the optimal ARIMA(0, 1, 0) parameters, the model was trained and tested. Residual diagnostics showed errors with a mean of zero, near-normal distribution, and no autocorrelation, indicating white noise. Performance metrics revealed an excellent model with a high R² score of 95.5% and a low RMSE of 0.41, reflecting strong predictive accuracy.
 
- *Predicting future values*
  - Using ARIMA(0,1,0) initially resulted in identical predictions and an increased AIC, though the sigma² coefficient decreased, indicating reduced noise. Despite explaining 88% of the variance, the RMSE of 1.20 was unsatisfactory due to significant fluctuations. Switching to ARIMA(0,2,0) improved alignment with the original data, reducing trends and seasonality. This approach resulted in predictions with a 95% confidence level and an improved RMSE of 0.40 cents, indicating a more accurate and practical forecast.
 
## Conclusion

The ARIMA(0,2,0) model improves prediction accuracy by addressing trends and seasonality, reducing RMSE, and capturing significant data variability. However, increasing data complexity over time may affect its accuracy, requiring further investigation to maintain long-term performance.



## References:

alkaline-ml.com. (2024). pmdarima.arima.auto_arima — pmdarima 1.5.3 documentation. [online] Available at: https://alkaline-ml.com/pmdarima/modules/generated/pmdarima.arima.auto_arima.html.

Brownlee, J. (2023). How to Create an ARIMA Model for Time Series Forecasting in Python. [online] Machine Learning Mastery. Available at: https://machinelearningmastery.com/arima-for-time-series-forecasting-with-python/ [Accessed 19 Apr. 2024].

matplotlib.org. (n.d.). matplotlib.gridspec.GridSpec — Matplotlib 3.7.1 documentation. [online] Available at: https://matplotlib.org/stable/api/_as_gen/matplotlib.gridspec.GridSpec.html [Accessed 24 Apr. 2024].

matplotlib.org. (n.d.). List of named colors — Matplotlib 3.4.2 documentation. [online] Available at: https://matplotlib.org/stable/gallery/color/named_colors.html [Accessed 24 Apr. 2024].

Numpy (2009). NumPy. [online] Numpy.org. Available at: https://numpy.org/. [Accessed 22 Apr. 2024].

OpenAI. (2024). ChatGPT (GPT-3.5 version) [Large language model]. https://chat.openai.com/chat (https://chat.openai.com/chat. [Accessed 24 Apr. 2024])

pandas.pydata.org. (n.d.). User Guide — pandas 1.0.4 documentation. [online] Available at: https://pandas.pydata.org/docs/user_guide/index.html#user-guide. [Accessed 22 Apr. 2024].

Python.org. (2019). statistics — Mathematical statistics functions — Python 3.7.2 documentation. [online] Available at: https://docs.python.org/3/library/statistics.html [Accessed 24 Apr. 2024].

Python Software Foundation (n.d.). Math — Mathematical Functions — Python 3.8.3rc1 Documentation. [online] docs.python.org. Available at: https://docs.python.org/3/library/math.html [Accessed 24 Apr. 2024].

Raval, P. (2024). How to Build ARIMA Model in Python for time series forecasting? [online] ProjectPro. Available at: https://www.projectpro.io/article/how-to-build-arima-model-in-python/544. [Accessed 16 Apr. 2024]

scikit-learn.org. (n.d.). sklearn.metrics.r2_score — scikit-learn 0.24.1 documentation. [online] Available at: https://scikit-learn.org/stable/modules/generated/sklearn.metrics.r2_score.html [Accessed 24 Apr. 2024].

Shumway, R.H. and Stoffer, D.S. (2017). ARIMA Models. In: Time Series Analysis and Its Applications. Springer, Cham, pp.75–163.

Statsmodels.org. (2010). statsmodels.tsa.stattools.adfuller — statsmodels v0.11.0dev0+265.gb3c5e2711 documentation. [online] Available at: https://www.statsmodels.org/dev/generated/statsmodels.tsa.stattools.adfuller.html [Accessed 24 Apr. 2024].

www.statsmodels.org. (n.d.). API Reference - statsmodels 0.15.0 (+270). [online] Available at: https://www.statsmodels.org/devel/api.html [Accessed 24 Apr. 2024].

www.statsmodels.org. (n.d.). statsmodels.graphics.tsaplots.plot_acf - statsmodels 0.15.0 (+59). [online] Available at: https://www.statsmodels.org/dev/generated/statsmodels.graphics.tsaplots.plot_acf.html [Accessed 24 Apr. 2024].

www.statsmodels.org. (n.d.). statsmodels.tsa.arima.model.ARIMA — statsmodels. [online] Available at: https://www.statsmodels.org/stable/generated/statsmodels.tsa.arima.model.ARIMA.html [Accessed 21 Apr. 2024].
