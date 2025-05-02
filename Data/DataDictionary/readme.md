# Data Dictionary

This document provides detailed information about all variables in the COVID-19, Mobility, and S&P 500 analysis dataset.

## Primary Variables

| Column Name | Data Type | Description | Example Value | Notes |
|-------------|-----------|-------------|--------------|-------|
| Date | date | Date of observation | 2020-03-15 | Format: YYYY-MM-DD |
| Value | float | S&P 500 index value | 2711.02 | Daily closing value |
| New_Cases | integer | Confirmed new COVID-19 cases | 3500 | Daily count for USA |
| New_Deaths | integer | New COVID-19 deaths | 63 | Daily count for USA |
| Is_trading_day | boolean | Indicates if date is a trading day | True | False on weekends and market holidays |

## Mobility Metrics (percent change from baseline)

| Column Name | Data Type | Description | Example Value | Notes |
|-------------|-----------|-------------|--------------|-------|
| Retail_and_recreation | float | Mobility change for retail and recreation locations | -25.3 | Percent change from baseline |
| Grocery_and_pharmacy | float | Mobility change for grocery and pharmacy locations | 10.5 | Percent change from baseline |
| Parks | float | Mobility change for parks | 35.2 | Percent change from baseline |
| Transit_stations | float | Mobility change for transit stations | -32.6 | Percent change from baseline |
| Workplaces | float | Mobility change for workplaces | -45.8 | Percent change from baseline |
| Residential | float | Mobility change for residential areas | 15.2 | Percent change from baseline |

## Derived Variables

| Column Name | Data Type | Description | Example Value | Notes |
|-------------|-----------|-------------|--------------|-------|
| New_cases_7d_avg | float | 7-day moving average of new cases | 3250.5 | Smooths daily fluctuations |
| New_cases_12d_avg | float | 12-day moving average of new cases | 3100.2 | Smooths daily fluctuations |

## Lagged Variables

| Column Name | Data Type | Description | Example Value | Notes |
|-------------|-----------|-------------|--------------|-------|
| New_Cases_lag1 | integer | New cases from previous day | 3200 | 1-day lag |
| New_Deaths_lag1 | integer | New deaths from previous day | 58 | 1-day lag |
| Retail_and_recreation_lag1 | float | Retail/recreation mobility from previous day | -24.1 | 1-day lag |
| New_Cases_lag3 | integer | New cases from 3 days ago | 2950 | 3-day lag |
| New_Deaths_lag3 | integer | New deaths from 3 days ago | 52 | 3-day lag |
| Retail_and_recreation_lag3 | float | Retail/recreation mobility from 3 days ago | -23.5 | 3-day lag |
| New_Cases_lag5 | integer | New cases from 5 days ago | 2800 | 5-day lag |
| New_Deaths_lag5 | integer | New deaths from 5 days ago | 48 | 5-day lag |
| Retail_and_recreation_lag5 | float | Retail/recreation mobility from 5 days ago | -22.8 | 5-day lag |
| New_Cases_lag7 | integer | New cases from 7 days ago | 2650 | 7-day lag |
| New_Deaths_lag7 | integer | New deaths from 7 days ago | 45 | 7-day lag |
| Retail_and_recreation_lag7 | float | Retail/recreation mobility from 7 days ago | -21.5 | 7-day lag |

*Note: Similar lag variables exist for all mobility metrics (Grocery_and_pharmacy, Parks, Transit_stations, Workplaces, Residential).*

## Data Quality Information

- **Missing Values**: Some missing values exist in recent rows and lagged features
- **Temporal Coverage**: Data spans from early 2020 through 2021
- **Spatial Coverage**: United States data only
- **Special Considerations**: Trading days vs. non-trading days need special handling when analyzing market relationships
