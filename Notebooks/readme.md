# Notebooks Directory

This directory contains Jupyter notebooks for the COVID-19, Mobility, and S&P 500 analysis project. These notebooks document the data collection, processing, analysis, and modeling steps.

## Notebooks

### 1. `cellis3_project_data.ipynb`

**Purpose**: Data collection, scraping, and merging

**Description**: This notebook handles all data acquisition and initial preparation, including:
- Web scraping COVID-19 data 
- Downloading mobility data from Google COVID-19 Community Mobility Reports
- Fetching S&P 500 index data from federal reserve
- Merging these disparate data sources into a unified dataset
- Initial data cleaning and formatting

**Key Sections**:
- Data source connections and API interactions
- Web scraping implementation
- Data alignment and merging logic
- Date handling and normalization
- Creation of the base dataset for analysis
- Export of the merged dataset to `data/raw/covid_mobility_sp500.csv`

**Dependencies**:
- pandas
- numpy
- requests
- matplotlib
- datetime

### 2. `cellis3_projectcheckin.ipynb`

**Purpose**: Initial visualizations, analysis, and modeling

**Description**: This notebook performs exploratory data analysis and initial modeling on the merged dataset, including:
- Data exploration and visualization
- Correlation analysis between COVID-19 metrics, mobility data, and S&P 500
- Feature engineering including creation of lagged variables
- Handling of trading vs. non-trading days
- Initial predictive modeling

**Key Sections**:
- Data loading and preprocessing
- Missing value analysis and handling
- Exploratory visualizations
- Statistical correlation analysis
- Time series analysis
- Feature importance evaluation
- Initial predictive models
- Evaluation of results and next steps

**Dependencies**:
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- statsmodels

## Running the Notebooks

The notebooks should be run in sequence:
1. First run `cellis3_project_data.ipynb` to generate the dataset
2. Then run `cellis3_projectcheckin.ipynb` for analysis and modeling

## Notebook Standards

- All notebooks include markdown cells explaining the purpose of each section
- Code includes comments for complex operations
- Visualizations include titles, labels, and legends
