# City Temperature Analysis and Forecasting

## Project Overview
This project is a comprehensive analysis and forecasting of temperature data across various cities worldwide using the `city_temperature.csv` dataset from Kaggle. The analysis is divided into two parts:
1. **Tabular Analysis** - Using PyCaret for regression modeling to understand relationships in temperature data.
2. **Time-Series Analysis** - Analyzing and forecasting temperature trends over time using time-series techniques.

## Dataset
**Dataset Name**: `city_temperature.csv`  
**Source**: [Kaggle](https://www.kaggle.com/datasets)  
**Description**: This dataset includes daily average temperatures for multiple cities across different countries and regions.

**Key Columns**:
- `Region`: Region of the city
- `Country`: Country of the city
- `State`: State (if available)
- `City`: City name
- `Month`, `Day`, `Year`: Date components
- `AvgTemperature`: Average temperature recorded on that day

## Project Methodology

### 1. Tabular Analysis
In this part, the dataset is treated as a tabular dataset to explore features and build predictive models using PyCaret’s AutoML capabilities.

- **Data Preprocessing**: Handling missing values, filtering out erroneous temperature readings, and feature engineering.
- **Exploratory Data Analysis (EDA)**: Understanding distributions, correlations, and patterns in the data.
- **Modeling with PyCaret**: Various regression models are compared using PyCaret’s `compare_models()` function to identify the best model for predicting average temperatures.

### 2. Time-Series Analysis
In the time-series analysis, the dataset is filtered and organized to perform trend analysis and forecasting.

- **Data Preparation**: Filtering data for specific cities or regions with sufficient data points, handling missing values, and setting up date indices.
- **Time-Series Decomposition**: Decomposing the series to understand seasonal, trend, and residual components.
- **Feature Engineering**: Adding lag features and date-based features (e.g., month, day of the week).
- **Modeling with PyCaret**: Setting up PyCaret for time-series regression modeling to forecast future temperatures.

## Setup and Dependencies

### Requirements
This project requires the following Python packages:
- `pandas`
- `numpy==1.21.0`
- `pycaret`
- `matplotlib`
- `statsmodels`

### Installation Instructions

To install dependencies:
```bash
!pip install numpy==1.21.0 pandas matplotlib statsmodels pycaret
```
## Run Instructions

### Clone the repository:
```bash
git clone <your-repo-link>
cd <repository-directory>
```
### Open the Colab notebooks:
You’ll find two Colab notebooks:

- **Tabular_Analysis.ipynb**: For the tabular analysis.
- **Time_Series_Analysis.ipynb**: For the time-series analysis.

### Upload Dataset:
Ensure the `city_temperature.csv` dataset is uploaded to the Colab environment before running the code cells.

### Run Cells:
Follow each notebook’s step-by-step cells to preprocess data, perform analysis, and build models.

## Project Structure

├── Tabular_Analysis.ipynb           # Notebook for tabular analysis and modeling with PyCaret

├── Time_Series_Analysis.ipynb       # Notebook for time-series analysis and forecasting

├── city_temperature.csv             # Dataset (not included due to size; download from Kaggle)

└── README.md                        # Project README

##Results
Tabular Analysis: The best model was selected using PyCaret’s compare_models(), providing a predictive baseline for temperature estimation based on available features.
Time-Series Analysis: A time-series regression model was built to forecast future temperatures, with a focus on seasonal and trend components observed in the data.
