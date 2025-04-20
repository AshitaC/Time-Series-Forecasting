# Web Traffic Time Series Forecasting

# Project Overview

This project focuses on forecasting future web traffic for approximately 145,000 articles on Britannica, using time series data from July 1, 2015, to December 31, 2016. The dataset includes daily view counts for each article, categorized by access type (all, mobile, desktop, spider). The goal is to develop accurate forecasting models, leveraging metadata and exogenous variables like campaign data to predict future traffic trends.

# Dataset

train_1.csv: Contains ~145k time series, each representing daily views for a specific article. Rows correspond to articles, and columns represent dates. Missing values may indicate zero traffic or unavailable data.

Exog_Campaign_eng.csv: Provides exogenous data for English-language pages, marking dates with campaigns or significant events (1 for campaign days, 0 otherwise).


# Technologies & Libraries

- Python 3.x
- Pandas, NumPy
- Matplotlib, Seaborn
- Facebook Prophet
- Scikit-learn
- Statsmodels 


# Project Structure

The analysis is implemented in a Jupyter Notebook (Web_Traffic_Time_Series.ipynb) and follows these steps:

Data Loading: Imports and processes the datasets using pandas.

Exploratory Data Analysis (EDA): Analyzes traffic patterns, missing values, and trends.

Data Preparation: Checks for stationarity and applies transformations (e.g., differencing) as needed.

Model Prediction: Uses time series models (e.g., ARIMA) with grid search to find optimal parameters (p, d, q).

Evaluation: Assesses model performance using MAPE and RMSE and visualize forecasts.

# Results

- Achieved a **MAPE** of **4.63%** and RMSE of 291.11 using **SARIMAX**, a 57% improvement over ARIMA’s RMSE of 682.64, by modeling weekly seasonality and campaign-driven spikes.

- Demonstrated robust forecasting for volatile web traffic, leveraging exogenous variables to capture external events.
