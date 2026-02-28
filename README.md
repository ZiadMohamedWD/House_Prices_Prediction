# Housing_price_prediction

🏡 House Prices Prediction Project
This project focuses on analyzing and predicting California housing prices using machine learning and data visualization techniques. It involves data cleaning, feature analysis, outlier handling, encoding, modeling, and evaluation.

📁 Dataset
The dataset used is California Housing Dataset, which includes housing data with features like:

longitude, latitude – Location coordinates.

housing_median_age, total_rooms, total_bedrooms, population, households, median_income

median_house_value – The target variable.

ocean_proximity – Categorical column describing proximity to ocean.

📊 Project Workflow
1. Importing Libraries
Used:

pandas, numpy for data handling.

matplotlib, seaborn for visualization.

2. Loading the Data
The dataset is read from a .csv file into a DataFrame.

python
Copy
Edit
df = pd.read_csv("housing.csv")
3. Initial Data Exploration
df.info() and df.describe() to understand structure and summary statistics.

df.head() and df.tail() to preview data.

Checked for duplicates and null values.

4. Data Cleaning
Handled missing values by filling total_bedrooms with the column's mean.

Verified that no nulls remain after imputation.

5. Data Visualization
Used visual tools to understand distribution and relationships:

Histograms and boxplots for detecting outliers.

Correlation heatmap for numerical relationships.

Bar plots for categorical features like ocean_proximity.

6. Outlier Detection and Removal
Applied:

IQR method and Z-score to identify outliers.

Winsorization technique to cap extreme values while preserving data integrity.

7. Feature Engineering
Combined features (e.g. rooms_per_household, bedrooms_per_room) for more insightful predictors.

Converted categorical variables (ocean_proximity) using encoding techniques.

8. Data Scaling
Standardized features using StandardScaler or normalized depending on model requirements.

Scaling was applied after data split to avoid data leakage.

9. Model Training
Tested several regression models:

Linear Regression

Decision Tree Regressor

Random Forest Regressor

10. Model Evaluation
Used metrics like:

Mean Squared Error (MSE)

Root Mean Squared Error (RMSE)

R² Score

Also used train/test split and cross-validation to validate results.

11. Saving the Model (Optional)
Model can be saved using joblib or pickle for deployment.

📈 Results
The best model was selected based on performance metrics, giving reliable predictions of median house values across different regions of California.

💡 Future Work
Apply hyperparameter tuning to improve existing models like XGBoost and CatBoost.

Add model explainability using tools like SHAP or LIME.

Deploy the model as a web app using Flask or Streamlit.

Integrate interactive dashboards (e.g., Plotly, Dash).

Evaluate model performance on live or real-time data if available.


