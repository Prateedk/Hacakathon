Problem Statement in Brief:
Given the data of Enery consumption of past 10 years, forecast the Energy required for the next 3 years.

Approach:
1. Started with analysing the trend and observed the clear correlation between "Energy" and "years" through data visualization.
2. Interpolate the "Energy" to deal with missing data.
3. Used the PolynomialFeatures and LinearRegression to learn the Trend.
4. Subtract this from orginal data.
5. Implemented multi-output Random Forest(RF) with 24 hours of data. Forecast as per RF.
6. Predict the Trend from forecasted o/p of RF with earlier learnt Regression Model.
7. Subtract this from forecasted o/p of RF.

Key Observations:
1. Started with XGBoost, this overfits the data and performed poorly on test set.
2. Tried experiments with SARIMA but again performed poorly on test set.
3. Did some experiments with LSTM based Neural Network but hypertuning was taking a long time. As per initial experiments, expecting much better results with LSTM RNN.
