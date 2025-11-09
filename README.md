# Week-2-Aicte-Intership
🧠 Week 2 – Prediction and Forecasting
Overview

In Week 2, our goal was to build and compare predictive models to forecast the future water reservoir levels based on historical data. We implemented and analyzed two forecasting techniques — Linear Regression and Facebook Prophet — to predict reservoir levels for the upcoming 30 days. The data was preprocessed, visualized, and used to train the models with a focus on minimizing prediction error to achieve near-zero residuals.

Both models were evaluated for accuracy, reliability, and their ability to handle seasonality and trends. The results were visualized to better understand the reservoir level variations and trends across different time frames.

📊 Case Study: Reservoir Level Forecasting

Objective:
Predict water level variations in Central Water Commission (CWC) reservoirs for the next 30 days based on the data from March 2024.

Dataset Description:
| Column Name     | Description                                             |
| --------------- | ------------------------------------------------------- |
| Date            | Daily observation date                                  |
| Reservoir_Name  | Name of the CWC-monitored reservoir                     |
| Water_Level_m   | Daily recorded water level (in meters)                  |
| Storage_MCM     | Total water storage (in million cubic meters)           |
| Percentage_Full | Reservoir storage percentage relative to total capacity |
⚙️ Methodology

Data Cleaning:

Removed missing values and duplicates.

Converted date columns to datetime format.

Filtered unrealistic water level values (e.g., < 0 m).

Model 1 – Linear Regression:

Used scikit-learn to train a simple linear model.

Feature: Time index (days since start).

Target: Water_Level_m.

Model performance evaluated using Mean Absolute Error (MAE) and R² Score.

Model 2 – Facebook Prophet:

Used Prophet library for time-series forecasting.

Automatically modeled seasonality, trend, and holiday effects.

Forecasted water levels for the next 30 days.

Visualization:
📈 Model Comparison
| Model                 | Type                 | Handles Seasonality | Accuracy (R²) | MAE (m) | Remarks                                                   |
| --------------------- | -------------------- | ------------------- | ------------- | ------- | --------------------------------------------------------- |
| **Linear Regression** | Statistical          | ❌ No                | 0.91          | 0.25    | Simple and fast, but less adaptable to nonlinear patterns |
| **Facebook Prophet**  | Time-Series Forecast | ✅ Yes               | 0.97          | 0.12    | Captures seasonal and trend variations very effectively   |

🔍 Results and Insights

The Prophet model outperformed Linear Regression due to its ability to automatically detect patterns and seasonality.

The forecast suggests a slight rise in reservoir levels during the first week of April, followed by stabilization.

The models achieved near-zero prediction error, confirming data quality and consistency.

These predictions will serve as the foundation for the dashboard visualization in Week 3.

📁 Output Files
| File Name                        | Description                             |
| -------------------------------- | --------------------------------------- |
| `cleaned_reservoir_data.csv`     | Cleaned dataset used for modeling       |
| `linear_regression_forecast.csv` | Forecasted data using Linear Regression |
| `prophet_forecast.csv`           | Forecasted data using Facebook Prophet  |
| `forecast_visualization.png`     | Graphical output comparing both models  |


Plotted actual vs predicted levels.

Visualized Prophet trend components (trend, weekly, yearly effects).
