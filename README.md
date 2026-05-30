# Analysis and Forecasting of Weekly Electricity Consumption Using ARIMA Model

This repository contains the dataset, notebooks, figures, and final report for the Time Series Analysis project.

## Project Title

**Analysis and Forecasting of Weekly Electricity Consumption Using ARIMA Model: Evidence from PJM East Electricity Load Data**

## Project Overview

This project analyzes and forecasts weekly electricity consumption in the PJM East region using an ARIMA-based time series approach. The original hourly electricity load data are cleaned, processed, and aggregated into weekly electricity consumption. Baseline forecasting models and ARIMA models are then compared using validation and test forecasting performance.

## Repository Structure

```text
data/
├── raw/
│   └── PJME_hourly.csv
└── processed/
    ├── weekly_pjme_consumption_processed.csv
    ├── train_weekly_pjme.csv
    ├── validation_weekly_pjme.csv
    ├── test_weekly_pjme.csv
    └── metadata.json

figures/
└── figures used in the report

notebooks/
├── 01_Data_Processing_EDA.ipynb
└── 02_Time_Series_Modeling.ipynb

report/
└── Time_Series_Analysis_Project.pdf
```

## Dataset

The original dataset is the **Hourly Energy Consumption** dataset from Kaggle, specifically the `PJME_hourly.csv` file.

Dataset source: https://www.kaggle.com/datasets/robikscube/hourly-energy-consumption

The original variable is `PJME_MW`, which measures hourly electricity load in megawatts (MW). In this project, the hourly data are aggregated into weekly electricity consumption by summing hourly load values within each week.

## Methodology

The project includes:

* Data cleaning and preprocessing
* Missing timestamp checking and interpolation
* Weekly aggregation of hourly electricity load
* Exploratory Data Analysis
* Train-validation-test split
* Naive and Seasonal Naive baseline models
* ARIMA model selection
* Final test forecasting
* Rolling one-step forecast check
* Residual diagnostics
* SARIMA extension check

## Main Result

The selected final model is **Weekly ARIMA(3,0,2)**.

Final multi-step test performance:

* MAE: 250,006.38 MWh
* RMSE: 332,071.75 MWh
* MAPE: 4.86%
* Forecast Accuracy: 95.14%

Rolling one-step forecast performance:

* MAPE: 4.45%
* Forecast Accuracy: 95.55%

## Files

* `notebooks/01_Data_Processing_EDA.ipynb`: data cleaning, preprocessing, weekly aggregation, and exploratory data analysis.
* `notebooks/02_Time_Series_Modeling.ipynb`: baseline models, ARIMA model selection, final forecasting, rolling forecast, residual diagnostics, and SARIMA check.
* `report/Time_Series_Analysis_Project.pdf`: final written report.
* `data/raw/PJME_hourly.csv`: original hourly PJME dataset.
* `data/processed/`: processed weekly datasets used for modeling.

## Author

Nguyen Manh Cuong
Course: Time Series Analysis
Lecturer: Tran Thi Ha


