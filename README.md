# Groundwater-Prediction
This project explores groundwater level prediction using exploratory data analysis (EDA), statistical tests, data preprocessing, and machine learning models. The notebook combines both time series analysis and regression-based predictive modeling.
he notebook:

Loads groundwater dataset (groundwater_data.csv).

Performs EDA and visualization.

Handles missing values and interpolation.

Conducts time series stationarity tests (ADF test).

Builds and evaluates a Random Forest regression model.

Analyzes feature importance for groundwater prediction.

🔹 Step-by-Step Breakdown
1. Data Import & Libraries

Libraries: pandas, numpy, matplotlib, seaborn, sklearn, statsmodels.

Dataset loaded: groundwater_data.csv.

📌 Key Features in Data:

Rainfall, Humidity, Min Temperature, Max Temperature

Groundwater levels: GT4717003, GT4730005

Date column

2. Data Cleaning

Converts Date column to datetime.

Handles missing values using SimpleImputer(strategy='mean').

Extracts temporal features:

Year, Month, Day

Season (Winter, Spring, Summer, Fall)

3. Exploratory Data Analysis (EDA)

Correlation Heatmap of numerical variables.

Distribution plots of groundwater levels.

Time-series trends for GT4717003 and GT4730005.

📊 Helps to identify relationships between climate factors and groundwater levels.

4. Handling Missing Values

Visualizes missing values via heatmap.

Implements linear interpolation for columns with gaps.

Compares original vs. interpolated time series to check consistency.

5. Time Series Suitability Check

Uses Augmented Dickey-Fuller (ADF) Test to check stationarity:

If p-value < 0.05 → series is stationary.

If not, differencing/transformation required.

Plots rolling mean and standard deviation for stability check.

6. Feature Selection & Splitting

Selected features: Rainfall, Humidity, Min Temperature, Max Temperature, Year, Month, Day

Target variable: GT4717003 (groundwater level)

Train-Test split: 80/20

7. Model Training – Random Forest

Trains RandomForestRegressor on training set.

Makes predictions on test set.

Evaluation Metrics:

Mean Squared Error (MSE)

R² Score

8. Feature Importance

Extracts importance scores from Random Forest.

Visualizes using bar plots.

Identifies which climate factors most influence groundwater levels.
