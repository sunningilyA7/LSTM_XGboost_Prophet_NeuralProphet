# LSTM_XGboost_Prophet_NeuralProphet



## LSTM to Predict Sales Volume
Long Short-Term Memory (LSTM) networks are a type of recurrent neural network (RNN) suitable for sequence prediction problems. LSTMs are particularly useful for tasks where there is a dependency in the input data over time. This makes them ideal for predicting sales volume, where past sales data can be indicative of future trends.

### Usage:
### Data Preparation: 
Sales data is sequenced in time (e.g., daily, monthly sales).
### Model Setup: An LSTM model is configured with layers suited to the complexity and volume of the data.
### Training: The model learns from historical sales data, where features might include past sales, dates, promotional activities, and other relevant factors.
### Prediction: The trained model predicts future sales volume for a set period based on the learned patterns in the data.


## XGBoost + Prophet to Predict Sales Volume


It is known that Prophet can effectively decompose time trends, and LSTM can incorporate additional information into training.

Similarly, if there is no time series, XGBoost can also be used to train other information for prediction. 

So, what if we include the time trends decomposed by Prophet as features in the training? 

Wouldn't this take both time trends and additional information into account?"


XGBoost (Extreme Gradient Boosting) is a powerful machine learning algorithm that uses gradient boosting framework. It is highly effective for regression, classification, and ranking problems. Prophet is a forecasting tool designed for handling time series data that displays patterns on different time scales such as yearly, weekly, and daily.

### Usage:

### Data Preparation: Sales data is prepared in a time-series format, with additional features that might influence sales volumes (like promotions, holidays).
### Prophet Model: Prophet is used to forecast the baseline sales volume based on time series patterns.
### XGBoost Model: XGBoost is used to correct or enhance the Prophet forecasts by learning from residuals (the differences between actual sales and Prophet predictions) and other features.
### Combined Training: The predictions from Prophet serve as input features to XGBoost, along with other data. XGBoost learns to predict adjustments or corrections to the initial forecasts.
### Prediction: The combined model outputs the final sales volume predictions, leveraging strengths from both Prophet’s time series decomposition and XGBoost’s learning capability.
### Each method offers a unique approach to handling time series prediction problems, utilizing different aspects of machine learning and statistical modeling to enhance predictive accuracy.





## NeuralProphet for Predicting Stock Price + Optuna
NeuralProphet is a machine learning library built on PyTorch that is based on Facebook's Prophet model but with neural network enhancements for improved forecasting capabilities. It's designed to handle time series data effectively with components to model trends, seasonality, and holidays.

Optuna is an automatic hyperparameter optimization software framework, particularly designed for machine learning tasks. It efficiently searches through multiple combinations of parameters to find the most effective settings.

### Usage:

### Data Preparation: Stock price data is structured in time-series format.
### Model Configuration: NeuralProphet is configured to predict future values of stock prices, considering potential daily, weekly, or annual patterns.
### Hyperparameter Tuning with Optuna: Optuna is used to optimize the NeuralProphet model parameters, such as learning rate, the number of layers, or other model-specific settings to improve accuracy.
### Training and Prediction: The optimized model forecasts future stock prices based on historical data, potentially incorporating external regressors like market indicators.

Data from https://www.kaggle.com/datasets/meetnagadia/netflix-stock-price-data-set-20022022






