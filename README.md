# Ontario House Price Prediction Analysis

This project analyzes Ontario property listings to explore geographic patterns in property prices and determine how well property prices can be predicted using location information.

## Project Objective

The project focuses on three main objectives:

- Explore how property prices vary across geographic areas in Ontario.
- Evaluate how well property prices can be predicted using area name, latitude, and longitude.
- Compare multiple regression models to identify the strongest predictive approach.

## Dataset

The dataset contains Ontario property listings with property prices, area names, and geographic coordinates.

The analysis includes data cleaning and validation for missing values, invalid prices, geographic coordinates, and duplicate records.

## Analysis & Modeling

The project includes:

- Data cleaning and validation
- Exploratory data analysis
- Geographic analysis of property prices
- One-hot encoding of categorical location data
- Linear Regression as a baseline model
- Random Forest Regression
- Gradient Boosting Regression
- Model comparison using MAE, RMSE, R², and Median Absolute Error

## Model Results

| Model | MAE | RMSE | R² | Median Absolute Error |
|---|---:|---:|---:|---:|
| Linear Regression | $348,238 | $783,445 | 0.121 | $190,658 |
| Random Forest | $292,680 | $778,651 | 0.131 | **$109,680** |
| Gradient Boosting | $352,719 | **$773,321** | **0.143** | $224,465 |

Random Forest produced the lowest typical prediction error based on Median Absolute Error, while Gradient Boosting achieved the highest R² and lowest RMSE.

## Key Findings

- Property prices vary substantially across geographic areas in Ontario.
- Location provides useful information about broad differences in property prices.
- Random Forest produced the lowest typical prediction error among the models tested.
- Location alone has limited ability to accurately predict the price of an individual property.
- Additional property characteristics such as size, property type, bedrooms, and bathrooms would likely be needed to build a stronger valuation model.

## Tools & Technologies

Python, pandas, NumPy, Matplotlib, Seaborn, Plotly, and scikit-learn.

## Repository Structure

- `data/` — Ontario property listing dataset
- `notebooks/` — Complete Jupyter Notebook analysis
- `README.md` — Project overview and key results

## Conclusion

Geographic location is related to property prices in Ontario, but location alone is not sufficient for accurate individual property valuation. Among the models tested, Random Forest provided the strongest typical prediction performance, while Gradient Boosting explained slightly more of the overall variation in property prices.
