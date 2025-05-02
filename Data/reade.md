# Data Directory

This directory contains all data files used in the COVID-19, Mobility, and S&P 500 analysis project.

## Structure

- `raw/`: Original, immutable data files
  - `cellis3_project_data.csv`: Main dataset containing COVID-19 statistics, mobility metrics, and S&P 500 values
  

## Data Sources

1. **COVID-19 Data**: From [COVID-19 Data Repository](https://www.worldometers.info/coronavirus/country/us/)
   - Collection period: 2020-2021
   - Focus: United States data
   - Variables: new cases, new deaths, and derived metrics

2. **Mobility Data**: From [Google COVID-19 Community Mobility Reports](https://www.google.com/covid19/mobility/)
   - Mobility metrics across different categories:
     - Retail and recreation
     - Grocery and pharmacy
     - Parks
     - Transit stations
     - Workplaces
     - Residential

3. **S&P 500 Data**: From [Fed Reserve](https://fred.stlouisfed.org/series/SP500)
   - Daily close values
   - Trading day indicators

## Processing Notes

The raw data undergoes the following processing steps:
1. Merging of multiple data sources by date
2. Creation of lagged variables (1, 3, 5, and 7 days)
3. Calculation of moving averages (7-day and 12-day)
4. Handling of missing values
5. Creation of trading day indicators

## Usage Notes

- Raw data should never be modified directly
- All processing steps are documented in the Jupyter notebooks
- When analyzing relationships, pay special attention to the alignment of dates, especially between trading and non-trading days
