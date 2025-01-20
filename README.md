# Time Series Analysis Project: Air Passengers Forecasting

This project demonstrates my **Time Series Data Analysis** skills by forecasting the number of airline passengers based on historical data. The dataset used in this project is the **AirPassengers** dataset, which contains monthly totals of international airline passengers from 1949 to 1960.

## Table of Contents
- [Overview](#overview)
- [Libraries and Tools Used](#libraries-and-tools-used)
- [Dataset](#dataset)
- [Steps and Methodology](#steps-and-methodology)
  - [Step 1: Data Preprocessing](#step-1-data-preprocessing)
  - [Step 2: Exploratory Data Analysis](#step-2-exploratory-data-analysis)
  - [Step 3: Stationarity Test](#step-3-stationarity-test)
  - [Step 4: Model Building](#step-4-model-building)
  - [Step 5: Forecasting](#step-5-forecasting)
- [Results](#results)
- [Conclusion](#conclusion)

## Overview
This project involves the **time series analysis** of monthly airline passenger data. The goal is to use this data to predict future trends and help make decisions about demand forecasting. The analysis was carried out in the following steps:

1. Data Preprocessing
2. Exploratory Data Analysis
3. Stationarity Test
4. Model Building using ARIMA and SARIMA
5. Forecasting

## Libraries and Tools Used
- `pandas` - Data manipulation and analysis
- `numpy` - Numerical operations
- `matplotlib` - Data visualization
- `statsmodels` - Time series modeling (ARIMA, SARIMA)
- `itertools` - Handling parameter combinations for grid search
- `sklearn` - Machine learning tools (though not used in the final model)
- `Jupyter` - Development environment for running the code

## Dataset
The dataset, **AirPassengers.csv** consists of the following columns:

- `Month` - The month of the data point
- `#Passengers` - The number of airline passengers in that month

## Steps and Methodology

### Step 1: Data Preprocessing
In this step, we read the data from a CSV file and convert the `Month` column to a `datetime` object. We set the `Month` column as the index and drop the original `Month` column.

### Step 2: Exploratory Data Analysis
We visualize the original time series data to identify any patterns, trends, or seasonality. We also calculate the rolling mean and standard deviation to observe the changes over time.

### Step 3: Stationarity Test
We perform the **Augmented Dickey-Fuller (ADF) Test** to check if the data is stationary. A stationary time series is one whose statistical properties such as mean and variance do not change over time. If the data is non-stationary, we apply a transformation (log transformation) and recheck for stationarity.

### Step 4: Model Building
We use **ARIMA (AutoRegressive Integrated Moving Average)** and **SARIMA (Seasonal ARIMA)** models to forecast the time series data. The process involves:
- Splitting the data into training and testing sets.
- Identifying the best ARIMA parameters using **Grid Search** based on AIC (Akaike Information Criterion).
- Fitting the ARIMA and SARIMA models and comparing their performance.

### Step 5: Forecasting
We forecast the number of airline passengers for the next 5 years (60 months) and plot the forecasted values alongside the original data for visual comparison.

## Results
The models were able to capture the trends and seasonality in the data, and the forecasted values provide insights into future passenger demand. The SARIMA model, which considers both trend and seasonality, produced more accurate results compared to the ARIMA model.

## Conclusion
This project showcases the process of time series forecasting using ARIMA and SARIMA models. The results demonstrate the ability to forecast future trends in airline passenger data, which could be applied in various industries for demand forecasting and capacity planning.
