# Bike Sharing Demand Forecasting

## Project Overview
This project focuses on analyzing and forecasting daily bike rental demand using the Capital Bikeshare dataset. The goal was to identify key drivers of demand (seasonality, weather, working days) and build predictive time series models to forecast future rentals.

The analysis demonstrates a complete Data Science workflow: from Exploratory Data Analysis (EDA) to advanced modeling using **SARIMAX**.

## Key Features & Methodology
* **Exploratory Data Analysis (EDA):** Visualizing trends, seasonality, and the impact of weather conditions using `ggplot2`.
* **Time Series Decomposition:** Breaking down data into trend, seasonal, and random components.
* **Stationarity Testing:** Using the Augmented Dickey-Fuller (ADF) test and differencing techniques.
* **Predictive Modeling:**
    * **Naive Method:** Baseline model.
    * **Auto ARIMA:** Univariate model based on historical data.
    * **SARIMAX:** Multivariate model incorporating exogenous variables (Temperature, Humidity, Windspeed, and Linear Trend).
* **Model Evaluation:** Comparing performance using RMSE, MAE, and MAPE metrics on a test set (Year 2012).

## Technologies Used
* **Language:** R
* **Libraries:** `ggplot2`, `forecast`, `tseries`, `dplyr`, `lubridate`, `plotly`, `knitr`.
* **Tools:** RStudio, RMarkdown.

## Results Summary
The analysis confirmed that bike rental demand is highly dependent on environmental factors.
* **Best Model:** The **SARIMAX** model (incorporating weather and trend) outperformed other models.
* **Key Insight:** Temperature is the strongest positive driver of demand, while high humidity and windspeed act as suppressors.
* **Challenge:** While the model accurately predicted daily fluctuations, it underestimated the record-breaking market growth in 2012, highlighting the need for dynamic trend updating in production environments.
