# "TOAZ" Payroll Fund Timeseries Forecasting Using SARIMA 



***STATUS:*** **Incomplete**


## Business Objectives:

All the data in the project is anonymized and does not reflect real figures. The project's objective was to develop an algorithm for predicting changes in the payroll fund at the "TOAZ" enterprise. The training data consisted of a complete time series from 2014 to 2024.

### Objectives:

1.	After analyzing the data, it was concluded that it is not necessary to divide the data into a test and training set; instead, the entire series should be used to train the model. Due to a significant jump in the payroll fund's change in 2024, transferring it to the training set may lead to incorrect algorithm performance.
2.	Based on the seasonality of the data, a SARIMA model was used.
3.	The validation data consisted of the data from the last three months, with the last month serving as a control assessment of the algorithm's performance.


## Research Conclusion:

Upon testing the algorithm's performance, the data from the first two months coincide with high accuracy, and the control result of the third month shows a specific accuracy of 96%, for the April i get around 82% of accuracy, total MAPE of the algorithm is near 12%. Thus, using the model, it is possible to predict results for four months ahead with high probability. Further validation will reveal how far and with what accuracy the algorithm predicts results.

Next, the image shows the constructed model, where the blue line represents the known data, and the green highlights indicate the predictions:

<img src="https://i.imgur.com/b0GCeot.png" alt="SARIMA"/>

We can see how the jump in 2024 has been established. If these data, along with some portion of 2023, were not included in the model training, the result would be significantly worse.

## Application of Research Results:

The results are ideal for building a strategy for the current year. If the model performs well in forecasting more than six months ahead, it can confidently be put into production.

## Technical Features of the Project:

Two approaches were considered for building the model. The first involved manual hyperparameter tuning, which required a deeper and more precise data analysis to find the variables p, d, q. This approach yielded good results compared to the next one. The second approach, the most convenient and fast, involved automatic hyperparameter search, which turned out to be the most optimal.


## Project Tools

- Python
- Pandas
- Statsmodels
- Pmdarima
- Dateutil
- Matplotlib.pyplot
