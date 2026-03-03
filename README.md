# California Housing: Geospatial EDA & Price Prediction

## Project Overview
This project applies Machine Learning to predict median house values across California districts. Using the 1990 Census dataset, I conducted a deep-dive Exploratory Data Analysis (EDA) to find spatial patterns and built a regression model to estimate property costs based on local demographics and geography.

## The Dataset
The dataset includes 20,640 records with features such as:
* **Geospatial:** Latitude and Longitude.
* **Property Specs:** Median house age, total rooms, and total bedrooms.
* **Demographics:** Population, households, and median income.
* **Target:** Median House Value (USD).

## Tech Stack
* **Analysis:** Python (Pandas, NumPy)
* **Visualization:** Matplotlib, Seaborn (Geospatial scatter plots, correlation heatmaps)
* **Machine Learning:** Scikit-Learn (Pipelines, Standard Scaling, Random Forest Regressor)

## Machine Learning Pipeline
1. **Data Cleaning:** Handled missing values in `total_bedrooms` and capped outliers.
2. **Feature Engineering:** Created ratios like `rooms_per_household` and `bedrooms_per_room` to improve model sensitivity.
3. **Preprocessing:** Applied **One-Hot Encoding** to categorical data (`ocean_proximity`) and **Standard Scaling** to numerical features.
4. **Model Selection:** Compared Linear Regression and Random Forest Regressors, using **Cross-Validation** to ensure model stability.

## Key Insights
* **The Income Factor:** Median income proved to be the strongest predictor of house prices ($r \approx 0.68$).
* **Location, Location, Location:** Geospatial analysis confirmed a massive price premium for coastal districts compared to inland areas.
* **Density Metrics:** Derived features (like population per household) revealed that crowded districts often have lower median values despite high total room counts.

## Performance
* **Primary Metric:** Root Mean Squared Error (RMSE)
* **Model:** Random Forest Regressor performed best, capturing non-linear relationships that simple linear models missed.
