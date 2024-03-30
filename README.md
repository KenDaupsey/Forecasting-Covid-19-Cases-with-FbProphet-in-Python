# Time Series Forecasting of Covid-19 Cases Using FbProphet in Python

## Introduction
This repository provides Python code for time series forecasting of Covid-19 cases using FbProphet. FbProphet is a forecasting tool that is designed for analyzing time series with daily observations that display patterns on different time scales.

## Installation
To install FbProphet, you can use pip:

```bash
pip install prophet
```

## Usage
The provided Python script demonstrates how to use FbProphet for forecasting Covid-19 cases. Here's a brief overview of the steps involved:

1. Load the dataset from the provided URL, which contains Covid-19 data for the US.
2. Preprocess the data by creating new columns for daily prevalence and filling any NaN values with 0.
3. Prepare the data for FbProphet by selecting the relevant columns and renaming them appropriately.
4. Define the FbProphet model and fit it to the prepared data.
5. Generate future dates for forecasting and predict the Covid-19 cases using the fitted model.
6. Plot the actual vs. forecasted deaths to visualize the predictions.
7. Display the forecast table, which includes the forecasted dates, trend, lower and upper confidence limits.

## Forecast Table and Confidence Limits
The forecast table contains the following columns:

- `ds`: The date for which the forecast is made.
- `trend`: The forecasted trend in Covid-19 deaths.
- `yhat_lower`: The lower bound of the forecasted Covid-19 deaths.
- `yhat_upper`: The upper bound of the forecasted Covid-19 deaths.

These bounds represent the uncertainty in the forecast and are based on the historical data and the model's parameters. The confidence intervals give insights into the range of possible outcomes, providing valuable information for decision-making and risk assessment.

## Example
```python
# Example usage of the provided code
import pandas as pd
from prophet import Prophet
import matplotlib.pyplot as plt

# Load dataset
url = 'https://raw.githubusercontent.com/nytimes/covid-19-data/master/us.csv'
df = pd.read_csv(url, parse_dates=['date'])

# Preprocess data...

# Define and fit the model...

# Generate forecast...

# Plot actual vs. forecasted deaths...

# Display forecast table...
```

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
```
This README provides an overview of the project, installation instructions, usage guidelines, explanation of the forecast table and confidence limits, an example usage snippet, and licensing information. Feel free to adjust it as needed for your repository.
