# COVID-19, Mobility, and S&P 500 Analysis

## Table of Contents
- [Project Overview](#project-overview)
- [Repository Structure](#repository-structure)
- [Data Dictionary](#data-dictionary)
- [Data Sources](#data-sources)
- [Analysis Files](#analysis-files)
- [Findings Summary](#findings-summary)
- [Challenges & Roadmap](#challenges--roadmap)

## Project Overview
This project analyzes the relationships between COVID-19 trends, mobility metrics, and the S&P 500 Index. The analysis explores how lagged values of COVID-19 cases and deaths correlate with market fluctuations, examines the impact of trading vs. non-trading days, and investigates connections between mobility data and both COVID-19 statistics and market performance.

## Repository Structure
```
DataWrangling/
├── data/                        # All data files
│   ├── raw/                     # Original, immutable data
│   │   └── covid_mobility_sp500.csv  # Main dataset with COVID-19, mobility, and S&P 500 data
│   ├── processed/               # Cleaned and processed data
│   └── README.md                # Documentation for data sources and processing
├── notebooks/                   # Jupyter notebooks for analysis
│   ├── cellis3_projectdata.ipynb    # Initial data exploration/cleaning
│   ├── cellis3_projectcheckin.ipynb # Analysis of relationships between variables
│   └── cellis3_FinalProject.ipynb   # Models for predicting S&P 500 values
├── visualizations/              # Generated charts and graphs
│   └── README.md                # Description of visualizations                
└── README.md                    # Main project README
```

## Data Dictionary
The complete data dictionary is available in `docs/data_dictionary.md`. Key variables include:

| Column Name | Data Type | Description | Example Value |
|-------------|-----------|-------------|--------------|
| Date | date | Date of observation | 2020-03-15 |
| Value | float | S&P 500 index value | 2711.02 |
| New_Cases | integer | Confirmed new COVID-19 cases | 3500 |
| New_Deaths | integer | New COVID-19 deaths | 63 |
| Is_trading_day | boolean | Indicates if date is a trading day | True |
| Retail_and_recreation | float | Mobility percent change from baseline for retail/recreation | -25.3 |

## Data Sources
The dataset is obtained from the following sources:
* COVID-19 data: [Worldometers](https://www.worldometers.info/coronavirus/country/us/)
* Mobility data: [Google COVID-19 Community Mobility Reports](https://www.google.com/covid19/mobility/)
* S&P 500 data: [Federal Reserve Economic Data (FRED)](https://fred.stlouisfed.org/series/SP500)

## Analysis Files
- `cellis3_projectdata.ipynb`: Initial data exploration, handling missing values, and data preparation
- `cellis3_projectcheckin.ipynb`: Analysis of relationships between COVID-19 metrics, mobility data, and S&P 500
- `cellis3_finalproject.ipynb`: Development of models to predict S&P 500 values using lagged variables

## Findings Summary
Initial analysis has revealed:
- Significant relationships between mobility metrics and S&P 500 data
- Patterns in how the market responds to changes in COVID-19 statistics
- Potential predictive value of lagged mobility and COVID-19 variables

## Challenges & Roadmap
Current challenges include:
- Missing data in recent rows and lagged features
- Ensuring correct alignment for lagged variables
- Consistency across trading/non-trading days

Next steps:
1. Finalize data cleaning and imputation for missing values
2. Update and finalize data dictionary
3. Expand visualizations and exploratory analysis
4. Conduct further feature selection and modeling
5. Interpret results and prepare final document
