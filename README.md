# Time-Series-Forecast
LSTM based price forecasting model for time series analysis.


Overview

In time series forecasting, the goal is to predict future values based on previously observed data. Traditional models like ARIMA or SARIMA capture linear trends and seasonal patterns, but they struggle with non-linear dependencies.

The LSTM model overcomes this by learning both short-term and long-term dependencies directly from the data, making it ideal for complex and noisy price signals.


#Project Workflow

1. Data Collection
Gathered datasets from multiple reliable sources:
Actual Sugar Prices (1962–2025)
ICE Sugar #11 Futures Data (2000–2025)
Crude Oil Prices (2000–2025)
Exchange Rates (USD, BRL, THB, INR, MYR to USD; 2004–2025)

2. Data Preprocessing & Feature Engineering
Standardized column names and unified date formats across all datasets.
Merged datasets into a single time-series dataframe using Date as the key.
Handled missing values with forward/backward fill.
Scaled features using MinMaxScaler to normalize input variables.
Created sequential time windows (past 60 days → next day) for model training.

3. Model Development (LSTM)
Built an LSTM (Long Short-Term Memory) model for sequence-based forecasting.
Trained using 80% of data and validated on the remaining 20%.
Captured long-term temporal dependencies between sugar price and external factors.


Compared LSTM-predicted prices with ICE Futures data to assess alignment.

